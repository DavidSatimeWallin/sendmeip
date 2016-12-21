# SendMeIP
SendMeIP is a small application that checks your public IP and sends an email if it changes. It also sends the IP every 5 hours even if it hasn't changed.

Simply install the package by writing ```go get -d github.com/dvwallin/sendmeip``` and then rename the example_config.yaml to config.yaml and place it in either /etc/sendmeip/ or $HOME/.sendmeip/ or in the directory where you run the application.

This is how the example config file looks like: 
```
refreshInterval: 5 # number of minutes between every check
mailSubject: New IP @ Home # the subject of the email you get
smtpHost: smtp.gmail.com # smtp host
smtpPort: 587 # smtp port
smtpUser: example@gmail.com # smtp username
smtpPass: ABC12345 # smtp password
notifyAddr: myEmailAddr@example.org # which address do you want the emails to go to?
```
