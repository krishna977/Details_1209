<h1>XSS in ATSPHP</h1>

<p>Enter something in the search feild as shown in Figure below</p>

<img src="https://raw.githubusercontent.com/krishna977/CVE_Details/master/atsphp/xss_0.PNG?token=AFCKSPR2Q273UY3HLVXCU6C5FRZJK" />

We can observe that the text is being reflected over the response so let us try to exploit it by closing input tag and adding  <pre>normal payload like <script> alert(0)</script> as shown in the Figure below </pre>

<img src="https://raw.githubusercontent.com/krishna977/CVE_Details/master/atsphp/xss_0_1.PNG?token=AFCKSPVGGTIXEWLJP7PM4MC5FR2SI" />

Clearly We can observe that script tag is being sanitized and just alert is being displayed so now ill try event handler payload like <pre>" onfocus="alert(document.domain)" autofocus="</pre>

<img src="https://raw.githubusercontent.com/krishna977/CVE_Details/master/atsphp/xss_1.PNG?token=AFCKSPXREJS22UU53KN7I2K5FR27A" />

Yeah i can see the XSS POPUP HA HA HA :)
