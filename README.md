# CODTECH-task1

### Name:PARTHEEBAN R

### Company:CODTECH IT SOLUTIONS

### ID:CTO8DS161

### Domain:CYBER SECURITY & ETHICAL HACKING

### Duration:june to july

### Mentor:SRAVANI GOUNI

# Password Strength Checker

This is a simple password strength checker implemented with HTML, CSS, and JavaScript. The application evaluates the strength of a password based on criteria such as length, presence of numbers, uppercase and lowercase letters, and special characters.

## Features

- Real-time password strength evaluation
- Visual feedback with different colors indicating password strength
- Easy to integrate and customize

## Getting Started

### Prerequisites

To run this project, you only need a web browser.

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/password-strength-checker.git
    ```
2. Navigate to the project directory:
    ```bash
    cd password-strength-checker
    ```

### Usage

1. Open the `index.html` file in your web browser.
2. Enter a password in the input field to see the strength evaluation in real-time.

## Code Overview

### HTML

The HTML structure consists of a container with an input field for the password and a paragraph for displaying the password strength.

```html
'<div class="container">
    <h1>Password Strength Checker</h1>
    <input type="password" id="password" placeholder="Enter password" oninput="checkPasswordStrength()">
    <p class="strength" id="strength"></p>
</div>'
 ```
# CSS

The CSS styles the container and the strength indicator. Different classes are used to indicate weak, medium, and strong passwords.

```css
.strength.weak {
    color: red;
}

.strength.medium {
    color: orange;
}

.strength.strong {
    color: green;
}
```

# javaScript

The JavaScript function checkPasswordStrength evaluates the strength of the password based on the following criteria:

Length of at least 8 characters
Contains lowercase letters
Contains uppercase letters
Contains numbers
Contains special characters
The strength is updated based on these criteria.

```javascript
function checkPasswordStrength() {
    const password = document.getElementById('password').value;
    const strengthText = document.getElementById('strength');
    let strength = 0;

    if (password.length >= 8) strength++;
    if (password.match(/[a-z]/)) strength++;
    if (password.match(/[A-Z]/)) strength++;
    if (password.match(/[0-9]/)) strength++;
    if (password.match(/[\W_]/)) strength++;

    if (strength === 0) {
        strengthText.textContent = '';
    } else if (strength < 3) {
        strengthText.textContent = 'Weak';
        strengthText.className = 'strength weak';
    } else if (strength < 5) {
        strengthText.textContent = 'Medium';
        strengthText.className = 'strength medium';
    } else {
        strengthText.textContent = 'Strong';
        strengthText.className = 'strength strong';
    }
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

Inspired by various password strength checking tools and tutorials available online.

# OUTPUT SCREENSHOT

![image](https://github.com/Partheeban37/CODTECH-task1/assets/144414138/97346a6f-6af2-4897-a5d5-a799d1bd7f36)

