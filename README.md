# MvcMusicStore-Tutorial
Microsoft ASP.NET MVC Music Store Tutorial

https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions/mvc-music-store/

Using Visual Studio 2015, ASP.NET 4.6.1

Notes:

1. In Part 4 of the Tutorial, the DbContext should be include `public DbSet<Artist> Artists {get; set'}`, or you won't be able to create the StoreManagerController

1. In Part 7, several modifications had to be made since MVC 5 uses ASP.NET Identity. When initially creating the project, "Individual User Accounts" Authentication was selected. So the scaffolding included the basic functionality for registering an account and loggging in. To add support for user roles, I followed the tutorial found at https://gooroo.io/GoorooTHINK/Article/17736/How-to-create-and-assign-roles-in-aspnet-mvc-5/32014#.XTNQ3uhKhhE. The tutorial instructions on adding an administrative user with the ASP.NET Configuration site do not apply to ASP.NET Identity.

1. In Part 8, while trying to create theShopping Cart Index page that is strongly typed to the ShoppingCartViewModel and uses the List View template, I initially got the error "Entity Type 'ShoppingCartViewModel' has no key defined. Define the key for this Entity type." This was resolved by entering a blank value for the "Data Context Class" when creating the view.
