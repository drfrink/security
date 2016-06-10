# Cross-site-scripting

Cross-site-scripting, or XSS as it is sometimes abbreviated to, is an attack that let's the attacker execute javascript code in the browser of the victim.

###So, what's the worst that can happen?
The attacker is probably not that interestd in changing the color or font of the website the victim is visiting. Although s/he could do that. The worst that can happen is probablt the following:

1. Session-hijacking/Cookie theft
This is when the attacker steals the cookie that is saved in the browser. Using this cookie the attacker can log in to the service as the victim, and thereby gain access to his/her account. If the victim is an admin that has extended privileges (uploading code, images, or whatever) this could lead to a compromise of the server itself.

2. Keylogger
The attacker can execute a keylogging-script that steals everything the user inputs in the website. This could be used to steal sensitive information, like passwords, credit cards information, chatlogs or whatever the user inputs.

3. Phishing
The attacker can insert a fake login. Image that you visit a site, and from that site you are able to login using your facebook or google-account. The attacker could spoof that so that when you enter your credencials, they are then sent to the attacker. 

### Types of XSS

1. Persistent
This is when the malicious code originates from the websites database. That means the attacker has managed to insert malicious code into the databse. So every time the database server that data the script will me executed.

2. Reflected
This is an attack where the script originates from the users request. This might seem a bit illogical, why would a user inject malicious code to himself? Well the code can 

### How does it really work?
Let's look at a practical example.


### Protect yourself

The problem with XSS is that it is a bit hard for the users to protect themselves. If there is a problem witht the website there is not that much the user can do.

One can always use noscript to block all javascript code. But that pretty much destroys the whole experience with using the internet.

### Protect your website
Of course the way to protect your website is to sanitize all input. 

You can also set the response-header like this:
`-xss-protection:"1; mode=block"`

For nodeJs you can use the helmet-module to do this.
https://www.npmjs.com/package/helmet


### Risks for the attacker
The obvious risk is that the attacker must expose a server. 

### Tools

#### BeeF XSS

###References:
http://excess-xss.com/
