# Section I 
## Write a mini test plan (comprised of 8-10 test cases) outlining how to sign up for Netflix and how to stream a movie or TV show 

### Verify the user can access the Site " Netflix" /com
     Open any browser 
     Enter https://www.netflix.com/login
    Verify users can  access the Netflix site 
  
### Verify sign up  functions appropriately 
    Enter https://www.netflix.com/login 
    Go to the bottom of the page 
    Verify the "sign up now" link- text is present on the page 
    Click on  sign up now link 
    Verify sign up link function and the user is redirected to the email login page 


### Verify the user can enter the valid email address on the email input field and Get Started functions appropriately.  
    Enter https://www.netflix.com/login 
    Go to the bottom of the page 
    Verify the "sign up now" link- text is present on the page 
    Click on  sign up now link
    On the email address field enter invalid email "test@gmail"
    Click Get Started Button 
    Verify error message displays below email input field stating " Please 
    enter a valid email address" 
    Again on the email address field enter the valid email address "johndoe@gmail.com"
    Click Get Started button 
    Verify the user is redirected to set up device page (https://www.netflix.com/signup/registration?locale=en-US)
 

 ### Verify email entered on the persist on the page and user can create a new password  
    Enter https://www.netflix.com/login 
    Go to the bottom of the page 
    Verify the "sign up now" link- text is present on the page 
    Click on  sign up now link
    On the email address field enter the valid email address "johndoe@gmail.com"
    Click Get Started button 
    Verify the user is redirected to set up device page (https://www.netflix.com/signup/registration?locale=en-US)
    Click Next button 
    Verify NEXT button functions and the user is redirected to create a password page (https://www.netflix.com/signup/regform) 
    Verify email entered step 5 "johndoe@gmail.com" persist on the page 
     Enter  valid password on the password field 
     Click Submit 
    Verify the user is redirected to choose a plan  page "https://www.netflix.com/signup"
    Click Next button 

  
### Verify user can select between three plans 
    Go to https://www.netflix.com/signup/planform 
    Verify 3 plan grid dialog box is present and the user can toggle between 3 plans 
    Click on the "Standard" dialog box 
    Verify user can toggle to the standard dialog box
    Click NEXT Button 
    Verify the user is redirected to the payment page  "https://www.netflix.com/signup/payment"
    Verify the user can select the desired payment plan 
    Go to https://www.netflix.com/signup/payment page 
    Verify  accordion is present on page  with three different options for payment 
    Click on Credit or DEbit accordion 
    Verify the user is directed to the credit/ debit setup page 
    https://www.netflix.com/signup/creditoption


### Verify the user can set up a monthly payment 
    Go to https://www.netflix.com/signup/creditoption 
    Enter the First name  from the debit card 
    Enter the Last Name from the debit card 
    Enter the Card number (16 digits) from the debit card 
    Enter Expiration date 
    Enter 3 digit CVV card number from the debit card 
    Enter the billing zip code 
    Verify the user can add all the values on the field. 
    Verify correct plan displays at the bottom of the form 
    Click the Start Membership button 
    Verify payment form successfully takes the user entry and navigates the user to 
    https://www.netflix.com/signup/otpPhoneEntry

### Verify the user can add a phone number 
    Go to https://www.netflix.com/signup/otpPhoneEntry 
    Enter the invalid phone number "571356764"
    Click the Text Me button 
    Verify user receives an error stating 
    "Sorry, we are unable to complete that action now. Please try again later."
    Enter the valid phone number "5713567640"
    Click the Text me button 
    Verify the user is directed to the code entry page  https://www.netflix.com/signup/otpCodeEntry 
    Verify the user can add validation code 
    Go to https://www.netflix.com/signup/otpCodeEntry
    Check the text message on the phone number user provided on /signup/otpPhoneEntry page 
    Enter the code on the text field 
    Click the Start Membership button 
    Verify user receives the "Welcome to Netflix" message 

### Verify the user can set up a password recovery phone number.
    https://www.netflix.com/simpleSetup/orderfinal
    Verify password recovery mobile text message is present 
    Enter the same phone as above 
    Click Next button 
    Verify page switches to https://www.netflix.com/simpleSetup/devicesurvey 

    Verify user can select multiple devices  
    Go to https://www.netflix.com/simpleSetup/devicesurvey
    Select all the icons eg: TV, Tablet, APP 
    Verify all the selected devices are highlighted with a red border 
    Verify all the selected devices are checked with a red checkmark 
    Click Next Button 
    Verify page switches to https://www.netflix.com/simpleSetup/newprofiles 
    Enter all the names of the people who will be sharing the account on the name field (optional)
    Click Next button 


### Verify Language checkbox functions on the secondary language page 

    Go to https://www.netflix.com/simpleSetup/secondarylanguages
    Search for secondary preferred language 
    Click on the check box next to the preferred language 
    Verify BLUE checkmark appears on next to the preferred language 
    Click NEXT Button 
    Verify the user is directed to the initial movie/ series page 
    Click on movies/ series title boxes ie: Schitts Creek 
    Verify  thumbs up icon displays on the title box 
 
### Verify the user is able to successfully search preferred movie or series 

    Go to https://www.netflix.com/browse
    Click the magnifying icon on the top right corner of the page 
    Verify search bar appears on the page after clicking a magnifying class
    Enter "Schitt's Creek" in the search bar 
    Verify Schitt's Creek"  filters and displays for the user to start watching the series 
   
  
   







# Section II 


### Once you find a bug, what is your preferred workflow? 

1. Create a sub-task in JIRA with the label "defect" or "bug". This helps in the team performance report. 

2. Write a short introduction to what the bug is about.

3. List all the browsers this affects. 

4. Enter very detailed steps as to how to reproduce the bug.

5. Enter the screenshot of the error you see on the page.

6. Click f12 to see if there is a javascript error. 

7. If applicable, add a screen recording of the bug.

8. List the severity of a bug. 

9. List a workaround if there is one.

10. Tag a developer who worked on the following story to put this on their radar. 

### If you were to test a login form that has a username, password, and a submit button, what are some inputs you would try in order to test edge cases? 


1. Enter the value as blank spaces on mandatory fields and click on the Save button

2. Test maximum and minimum character limit on both user name and password fields 

3. Test scenario for XSS attacks on the login page 

   3.1 Reflected XSS on User ID or Password field 

        <script>function(send_user_id)</script> 

    3.2 DOM XSS

4.  Test user cannot log in with only Special Character & Numbers (no letter) on both user name and password.

5.  Test the tab button cycles through the username, password, and save button for user convenience 

### How would you go about automating test scripts into a build pipeline? 
    Keep tests scoped to a single purpose. Each test should only do one Task 

    Build for reusable parts, with atomic, clear naming conventions.

    Separate each environment. Dev, Staging,and PROD. Code only moves after passing each environment 
    DEV---> Staging ---> PROD 


    Never use sleep the process. This slow down the build and might cause the build to fail 

    Any time application is changed, prepare for the change and monitor the build. 



# Pratical 
## Language Used: C# 

```C#
# For successful Login 

 public Loginpage EnterUserName()
        {
           var userNameTextField = Driver.Instance.FindElement(By.XPath("//input[@name='uname']"));
           userNameTextField.SendKeys("test");
           return this;
        }



        public Loginpage EnterPassword()
        {

            var passwordTextField = Driver.Instance.FindElement(By.XPath("//input[@name='pass']"));
           
            passwordTextField.SendKeys("test");

            return this;
        }


        //This method validates user name and password is added to the field 

        public Loginpage ValidateUserNameAndPassword()
        {
            string actualUserName = Driver.Instance.FindElement(By.XPath(""//input[@name='uname']")).Text.ToString().Trim();
            string expectedUserName = "test";
            Assert.AreEqual(actualUserName , expectedUserName);

           string actualPassword = Driver.Instance.FindElement(By.XPath("//input[@type='password']")).Text.ToString().Trim();
            string expectedPassword = "test";
            Assert.AreEqual(actualPassword , expectedPassword);
            
            return this
         }
     
   // This method click the login button 

    public void ClickLogInButton()
        {
            var loginButton = Driver.Instance.FindElement(By.XPath("//input[@type='submit']"));
              loginButton.PressButton();
            return this;
        }


   # For un-successful Login 
     public Loginpage EnterPassword()
        {

            var passwordTextField = Driver.Instance.FindElement(By.XPath("//input[@name='uname']"));
             passwordTextField.ClearAndEnterText("rest");
             return this;
        }

   
        public Loginpage EnterPassword()
        {

            var passwordTextField = Driver.Instance.FindElement(By.XPath("//input[@name='pass']"));
             passwordTextField.ClearAndEnterText("rest");
            return this;
        }

