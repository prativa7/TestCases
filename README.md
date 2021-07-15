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



# Pratical 

```
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

