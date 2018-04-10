# Asp.NetCoreAJAX

Demo of how to make AJAX call in Asp.Net Core 2 using razor pages

To get AJAX calls working like previous versions of MVC, you would need [jQuery Unobtrusive Ajax](https://github.com/aspnet/jquery-ajax-unobtrusive)

Once the js file is included in your code, you can use data-ajax* attributes to make ajax call

    <script src="~/js/jquery.unobtrusive-ajax.js"></script>

Example:

    <form action="/Time" method="get"
                  data-ajax-update="#Results" data-ajax-mode="REPLACE"
                  data-ajax="true" data-ajax-method="GET">
      <div class="py-3">
        <div id="Results">Place holder will be replaced by time when you click the button</div>
      </div>
      <input type="submit" value="Get time" class="btn btn-primary" />
    </form>

Complete mapping of each AjaxOptions with new HTML attribute can be found here:
[jQuery Unobtrusive Ajax Helpers in ASP.NET Core](https://dotnetthoughts.net/jquery-unobtrusive-ajax-helpers-in-aspnet-core/)
