Flutter Auth UI — Login & Sign Up Screens
A simple application developed using Flutter, containing two main screens:

The Login Page
<img width="962" height="911" alt="Image" src="https://github.com/user-attachments/assets/e6609b44-e71c-4904-8e40-c45c5019f381" />

The Sign Up Page
<img width="958" height="915" alt="Image" src="https://github.com/user-attachments/assets/dc58fd03-e265-460f-93da-537ee15f52d4" />

├── main.dart           # The entry point of the app and route definitions
├── login.dart          # The login screen UI
└── sign up.dart        # The sign-up (account creation) screen UI

Navigation between screens using Named Routes.

Use of input fields (TextFields) with proper styling.

Elegant user interface design using widgets like Column, Row, Padding, SizedBox, and more.

 Category                Widgets                                                                                        
 ----------------------  ---------------------------------------------------------------------------------------------- 
 **Core Structure**      `MaterialApp`, `Scaffold`, `AppBar`                                                            
 **Layout & Styling**    `Center`, `Column`, `Row`, `Padding`, `SizedBox`, `SingleChildScrollView`                      
 **Input Fields**        `TextField` with `InputDecoration` and `OutlineInputBorder`                                    
 **Buttons**             `ElevatedButton`, `TextButton`                                                                 
 **State & Navigation**  `StatefulWidget`, `StatelessWidget`, `Navigator` (with `pushNamed` and `pushReplacementNamed`) 

 Navigation Between Screens
The initialRoute and routes were defined in the main.dart file to control navigation between the screens:
نسخ
تحري
initialRoute: '/Login',
routes: {
  '/sign Up': (context) => const MyHomePage(title: 'sign Up'),
  '/Login': (context) => const LoginPage(),
}
From the Login Page ➜ Sign Up Page:
نسخ
تحرير
Navigator.pushReplacementNamed(context, '/sign Up');
From the Sign Up Page ➜ Login Page:
نسخ
تحرير
Navigator.pushNamed(context, '/Login');
