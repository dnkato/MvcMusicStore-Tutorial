# MvcMusicStore-Tutorial
The Microsoft ASP.NET MVC Music Store Tutorial is a well known sample ASP.NET MVC project that can be found at:

https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions/mvc-music-store/

However, this tutorial was written in 2011 using MVC 3 and a lot has changed since then.

As an excercise to learn about MVC, I decided to try my hand at coding this tutorial using Visual Studio 2017 and ASP.NET 4.6.1, MVC version 5.2.4.0.

Notes:

1. In Part 1, when initially creating the project, "Individual User Accounts" Authentication was selected so the scaffolding included the basic functionality for registering an account and loggging in (needed for part 7).

1. In Part 4 of the Tutorial, the DbContext should be include `public DbSet<Artist> Artists {get; set'}`, or you won't be able to create the StoreManagerController

1. In Part 7, several modifications had to be made since MVC 5 uses ASP.NET Identity. To add support for user roles, I followed the tutorial found at https://gooroo.io/GoorooTHINK/Article/17736/How-to-create-and-assign-roles-in-aspnet-mvc-5/32014#.XTNQ3uhKhhE. Please note that "ASP.NET Configuration site" instructions seen in older versions of the MVC Music Store tutorial does not apply to ASP.NET Identity.

1. In Part 8, while trying to create theShopping Cart Index page that is strongly typed to the ShoppingCartViewModel and uses the List View template, I initially got the error "Entity Type 'ShoppingCartViewModel' has no key defined. Define the key for this Entity type." This was resolved by entering a blank value for the "Data Context Class" when creating this view (and all subsequent views).

1. In Part 9, login uses email, not name. so the correct statement is `MigrateShoppingCart(model.Email);`

To Do:

* Style the site using bootstrap so that it looks closer to the original demo
