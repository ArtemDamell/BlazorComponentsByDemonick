## This is a toast component for Blazor Server, created by the author in 2021.

The component uses the System.Timers namespace and includes several methods for displaying toast messages with different status codes, such as SuccessfulMessage(), WarningMessage(), and ErrorMessage(). The component also includes a method ChooseMessageWithStatusCode() that allows the user to choose a message based on a specific status code.

When a message is displayed, the component adds a demonick-toast class to the containing div element and uses CSS classes to apply different background colors and icons for different message types.

The component also includes a timer that automatically closes the message after a set amount of time, which can be customized by changing the Interval property of the timer.

Overall, this is a useful component for displaying toast messages in a Blazor Server application.

# Toast Component:  
**1. Add the component in Shared or another folder**  
**2. Add the CSS file in wwwroot/css and include in _Host.cshtml** _(e.g. link href="css/demonick_toast.css" rel="stylesheet" )_  
**3. Add image folder in wwwroot/demonick_toast_images**  
**4. Add the component in page** _(e.g. <AlertComponent @ref="@alert" />)_  
**5. Initialize AlertComponent class** _(e.g. AlertComponent alert; )_  
**6. Use calling method for showing alert**  
_(e.g.  
            alert.ChooseMessageWithStatusCode(1, "Header message", "Body message");  
**or**  
            alert.SuccessfulMessage("Header message", "Body message");  
**or**  
            alert.ErrorMessage("Header message", "Body message");  
**or**  
            alert.WarningMessage("Header message", "Body message");   
    )_  

**Status codes:**  
1 - Successfull message alert  
2 - Warning message alert  
3 - Error message alert  
