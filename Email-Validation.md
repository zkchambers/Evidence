# Email Validation for Join Us Forms

![Email Validation](images/Email-Validation.png)

Code:
```
<input>type="email" class="form-control" placeholder="example@company.com" pattern="^([a-zA-Z0-9_\-\.]+)@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.)|(([a-zA-Z0-9\-]+\.)+))([a-zA-Z]{2,4}|[0-9]{1,3})(\]?)$" size="30" id="email" name="email" required</input>
```

I created a pattern for the email input field tp ensure that it includes a valid domain extension such as .com, .org, .edu etc. If the email that is inputted into the form that doesn't meet the criteria they will be prompted to fill it out correctly.
I had to find a pattern, understand how it worked. I had to test different emails and combinations to ensure that it works the way I want it to work. With this pattern it will ensure that all invaild emails will not work with the form and be sent to us. 