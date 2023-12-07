## Monu Otp Text Field

A Flutter package for creating an OTP (One-Time Password) input field with customization options. This package provides an easy-to-use widget for capturing OTP codes in your Flutter applications.

# Output 
https://github.com/Hasib74/monu_otp_text_field/assets/45905451/e4e0cc37-fb6c-474a-8955-e197ec32b0fe



# Installation
Add the following to your pubspec.yaml file:

```
dependencies:
  monu_otp_field:
    git:
      url: https://github.com/Hasib74/monu_otp_text_field.git
      ref: dev
```

# Then run:

flutter pub get


# Example
```
import 'package:monu_otp_field/monu_otp_field.dart';


MonuOtpTextField(
  numberOfFields: 6,
  borderColor: Theme.of(context).colorScheme.primary,
  showFieldAsBox: false,
  filled: true,
  cursorColor: Theme.of(context).colorScheme.primary,
  handleControllers: (List<TextEditingController?>? controllers) {
    // Do something with the controllers
    // e.g., concatenate the OTP values
  },
  onCodeChanged: (String code) {
    // Handle validation or checks here
    print("The OTP current code is: $code");
  },
  onSubmit: (String verificationCode) async {
    // Handle the submitted OTP
    // e.g., make an API call and proceed to the next step
  },
),

```

# Widget Properties
numberOfFields: Set the number of OTP input fields.
borderColor: Customize the color of the input field border.
showFieldAsBox: Choose to show the input field as a box (true) or as a dash (false).
filled: Decide whether the input field should be filled.
cursorColor: Set the color of the cursor.
handleControllers: Use this callback to work with the list of TextEditingController instances.
onCodeChanged: Implement this callback for when the OTP code changes.
onSubmit: Define this callback for when all fields are filled, and the OTP is submitted.


# Customization

Feel free to personalize the appearance of the OTP input field using the available properties. You can modify the border, cursor, and other visual aspects to match your app's design.

```
MonuOtpTextField(
  // ... other properties
  decoration: InputDecoration(
    border: OutlineInputBorder(
      borderRadius: BorderRadius.circular(10.0),
      borderSide: BorderSide(color: Colors.red), // Customize the border color
    ),
    fillColor: Colors.blue, // Customize the fill color
    filled: true,
  ),
),

```

