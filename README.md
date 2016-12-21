# SendMeIP
SendMeIP is a small application that checks your public IP and sends an email if it changes. It also sends the IP every 5 hours even if it hasn't changed.

## Install
```go get -d github.com/dvwallin/sendmeip``` 
```cd $GOPATH/src/github.com/dvwallin/sendmeip```
```go install```
```mkdir $HOME/.sendmeip && cp example_config.yaml $HOME/.sendmeip/config.yaml```

Now edit $HOME/.sendmeip/config.yaml and set the parameters to whatever you want.
The config.yaml can be placed in either /etc/sendmeip/ or $HOME/.sendmeip/ or in the directory you're in when running the application.

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
