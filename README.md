# 2-Faktor Authentifizierung (2FA) im WordPress CMS

## Überblick

* Funktionalität
* WordPress
* Apps für Android und iPhone


> https://en.wikipedia.org/wiki/Google_Authenticator

## Funktionalität
Die WordPress Login Maske wird um ein drittes Eingabefeld erweitert. Dort wird ein Time Based One Time Passwort (TOTP) für eine zusätzliche Kontrolle eingegeben. Dieses TOTP wird mittels App berechnet.

![OTP1 logo](http://christophwolff.de/br/screenshots/OTP1.png)

### Einstellungen
Um die App zu registrieren, wird das Benutzerprofil im Backend am Ende um die Google Authenticator Settings erweitert.

![OTP1 logo](http://christophwolff.de/br/screenshots/OTP2.png)

Folgende Einstellungen müssen Sie als Autor vornehmen:

* **Activate**

  Der Hakten aktiviert die 2 Faktor Authentifizierung für Ihren Nutzer
  
* **Get QR Code**
  
  Hier wird der QR Code für den Anmeldeprozess auf dem Smartphone angezeigt. (s.u.)
  
* **Recovery Codes**
	
  Dieser Code hilft Ihnen, wenn Sie das Smartphone nicht zu Hand haben, sich aber trotzdem anmeldem müssen.

## Google Authenticator (Android und iOS)

Das TOTP, welches bei jedem Login eingegeben werden muss, wird über eine App generiert. Der Google Authenticator. **Es werden weder Daten an die Google Server übertragen, noch ist ein Google Account erforderlich!**

Android:

[Google Authenticator (Google Playstore)] (https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2) | [http://bit.ly/google-auth-android](http://bit.ly/google-auth-android)

iOS:

[Google Authenticator (AppStore)] (https://itunes.apple.com/en/app/google-authenticator/id388497605?mt=8) | [http://bit.ly/google-auth-ios](http://bit.ly/google-auth-ios)

In der App kann entweder über einen Barcode Scanner der *QR-Code* eingescannt oder der *Secret* eingegeben werden. Dieses Verbindet die App über den Zeitgesteuerten Algorthmus mit dem WordPress CMS. 

<figure>
<img style="width:50%;float: none;" src="http://christophwolff.de/br/screenshots/gaimage.jpg">
<figure-caption>Das TOTP ist nur für ein paar Sek. gültig</figure-caption>
</figure>

**Tipp**: Es sind noch weitere Apps (Windows, Mac OS X, ..) die diesen Prozess abbilden verfügbar. Stichwort: TOTP. Es wurde der Einfachheit halber aber hier nur auf den Google Authenticator eingegangen. 


*Weiter führende Informationen:*

> TOTP: Time-Based One-Time Password Algorithm
> 
>>http://tools.ietf.org/html/rfc6238
>
>>http://garbagecollected.org/2014/09/14/how-google-authenticator-works/
>
>>http://www.techrepublic.com/blog/google-in-the-enterprise/use-google-authenticator-to-securely-login-to-non-google-sites/
