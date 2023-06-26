# C sharp-based CAPTCHA solver ([Metabypass](https://metabypass.tech))
Free demo (no credit card required) -> https://app.metabypass.tech/application


## Configuration

Get the credentials from the [Application](https://app.metabypass.tech/application) section of the MetaBypass website:

1. Go to [Application Section](https://app.metabypass.tech/application)
2. You can see credentials like the below image



![Uploading 239733451-4420f7ed-1588-412a-b0e8-2876d4ae1854.png…](https://github.com/metabypass/metabypass-python/assets/128980891/4420f7ed-1588-412a-b0e8-2876d4ae1854)


 ## Implementation:
To obtain the results for each type of captcha, do the following steps:
   1. Create a C# Console Application
     
   2. Download **meyabypass-csharp.dll** and **token.txt** files.
     
   3. In the Solution Explorer, right-click on the "References". Select "Add Reference". Click on the "Browse" button to navigate to the location where you have the **meyabypass-csharp.dll** file.
      
   4. Put **token.txt** in YOUR_SOlUTION_PATH/bin/debug
      
   5. In **Program.cs** write following codes for each type of captcha
       - **Text_Captcha**
     
         ```csharp
         using System;
         
         namespace YOUR_NAME_SPACE
         {
             class Program
             {
                 static void Main(string[] args)
                 {
                     metabypass_csharp.Program.ClientId = "YOUR_CLIENT_ID";
                     metabypass_csharp.Program.ClientSecret = "YOUR_CLIENT_SECRET";
                     metabypass_csharp.Program.Username = "YOUR_ACCOUNT_EMAIL";
                     metabypass_csharp.Program.Password = "YOUR_ACCOUNT_PASSWORD";
                     
                     var res = metabypass_csharp.Program.TextCaptcha(metabypass_csharp.Program.ImageToBase64("YOUR_CAPTCHA_IMAGE_PATH"));
                  
                     Console.WriteLine(res);
                     Console.ReadKey();
                 }
             }
         }

         ```
       
       - **Recaptcha V2**
    
         ```csharp
         using System;
         
         namespace YOUR_NAME_SPACE
         {
             class Program
             {
                 static void Main(string[] args)
                 {
                     metabypass_csharp.Program.ClientId = "YOUR_CLIENT_ID";
                     metabypass_csharp.Program.ClientSecret = "YOUR_CLIENT_SECRET";
                     metabypass_csharp.Program.Username = "YOUR_ACCOUNT_EMAIL";
                     metabypass_csharp.Program.Password = "YOUR_ACCOUNT_PASSWORD";
         
                     var res = metabypass_csharp.Program.RecaptchaV2("YOUR_SITE_KEY", "YOUR_SITE_URL");
         
                     Console.WriteLine(res);
                     Console.ReadKey();
                 }
             }
         }
       
       - **Recaptcha V3**
    
         ```csharp
         using System;
         
         namespace YOUR_NAME_SPACE
         {
             class Program
             {
                 static void Main(string[] args)
                 {
                     metabypass_csharp.Program.ClientId = "YOUR_CLIENT_ID";
                     metabypass_csharp.Program.ClientSecret = "YOUR_CLIENT_SECRET";
                     metabypass_csharp.Program.Username = "YOUR_ACCOUNT_EMAIL";
                     metabypass_csharp.Program.Password = "YOUR_ACCOUNT_PASSWORD";
         
                     var res = metabypass_csharp.Program.RecaptchaV3("YOUR_SITE_KEY", "YOUR_SITE_URL");
         
                     Console.WriteLine(res);
                     Console.ReadKey();
                 }
             }
         }
       
         ```

