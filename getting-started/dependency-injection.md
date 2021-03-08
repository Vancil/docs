# Dependency Injection

You can use dependency injection to bring classes from the package into your application.  You can configure your container in your _Startup.ConfigureServices_ method:

```aspnet
public class Startup {
  public void ConfigureServices(IServiceCollection services) {
    services.AddTransient<IStringHelper, StringHelper>();
  }
  // ...
}
```

When a request gets routed to your controller, it will be [resolved from the container](https://github.com/aspnet/Mvc/blob/eeac99985a61e75ca48e620f0371e16df018d6d7/src/Microsoft.AspNetCore.Mvc.Core/Controllers/ServiceBasedControllerActivator.cs#L16-L26) along with all its dependencies:

```aspnet
public class BooksController : Controller {

  private readonly IStringHelper _stringHelper;
  
  public BooksController(IStringHelper stringHelper) {
    _stringHelper = stringHelper;
  }
 
  [HttpGet]
  public async Task<IActionResult> GetBookTitleBase() 
  {
    var titleBase = _stringHelper.Before("Harry Potter and the Half-Bloog Prince", "and")
    // titlbase = "HarryPotter"
  }
}
```

