# Automate applying for housing in housing connect

Open housing connect website and paste the below code in devtool console.

```javascript
setInterval(() => {
  let applyButtons = document.getElementsByClassName("button");
  for (let i = 0; i < applyButtons.length; i++) {
    if (applyButtons[i].innerText === "Apply") {
      applyButtons[i].click();
      break;
    }
  }
  setTimeout(() => {
    let emailBox = document.getElementsByClassName("gwt-TextBox");
    emailBox.Email.value = "YOUR_EMAIL_ADDRESS";
    let passwordBox = document.getElementsByClassName("gwt-PasswordTextBox")[0];
    passwordBox.value = "YOUR_SUPER_SECURE_PASSWORD";
    passwordBox.click();
    document.getElementsByClassName("button")[2].click();
  }, 2000);
  setTimeout(() => {
    document.getElementsByClassName("button")[0].click();
  }, 2000);
}, 3000);
```
