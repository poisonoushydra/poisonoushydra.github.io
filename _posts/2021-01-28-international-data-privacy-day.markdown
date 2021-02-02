---
layout: post
title:  "International Data Privacy Day"
date:   2021-01-28
categories: jekyll update
---
Today is International Data Privacy Day so I would like to take this opportunity to share some information with my fellow Internet users in hopes that it will help some of you become more knowledgeable regarding the types of data which are being harvested from your devices, for the most part without your knowledge or consent. I will try to make this as accessible as possible by using terms and concepts that a layperson can easily grasp but please feel free to comment or message me privately if you have any questions or concerns that are not covered by this post.

# Google

A good place to start is to reduce or eliminate your dependency on Google as they are known to be one of the biggest offenders regarding data privacy. Most of us are guilty of over-using their services, especially those of you using Android as your mobile platform of choice. This can be a difficult one but every little bit helps. If you find it impossible to stop using Google as a search engine at the very least consider visiting the following URL and disabling the three options for 
<a href="https://myactivity.google.com/myactivity?pli=1" onclick="window.open('https://myactivity.google.com/myactivity?pli=1', '_self');">
Web & Web Activity, Location History, and YouTube History 
</a>. It is also worth considering signing out of your Google account when performing searches or doing so in Incognito mode to limit the amount of tracking you are subjected to. Consider using <a href="https://duckduckgo.com" onclick="window.open('https://duckduckgo.com', '_self');">
DuckDuckGo</a> as a privacy-respecting alternative to Google either via their website or by changing the default search engine in your browser. 

# Email

Gmail can also be a difficult one to let go of but there are plenty of alternatives available these days. The two I personally use are <a href="https://webmail.vivaldi.net" onclick="window.open('https://webmail.vivaldi.net', '_self');">
Vivaldi Webmail</a> and <a href=" https://mail.tutanota.com" onclick="window.open('https://mail.tunanota.com', '_self');">
Tutanota</a>. Vivaldi Webmail offers 5GB of free storage, and Tutanota offers 1GB which should be plenty for most users. They both offer end-to-end encryption of messages if you need to send email with an added layer of security. Encrypting and decrypting email messages is beyond the scope of this article, however. Both services also do not load images by default. This is because many organizations now use tracking pixels (invisible 1X1 images embedded in email messages) to notify them as soon as you read an email message. 

# Browsing 

Google Chrome currently accounts for an estimated 66% of all web traffic. This is troublesome for many reasons but primarily for the fact that Google is in the business of data brokerage. This means that they monetize your data and sell it to the highest bidder. Google Analytics are now used by the majority of sites you visit on a daily basis allowing Google to build a robust profile of virtually everything you access online. I personally use [Vivaldi](https://vivaldi.com/ "Vivaldi") as my daily browser. It offers much more customization and configuration than Chrome and has a much more transparent privacy policy. It does still collect and share some information about your device with servers in [Iceland](https://vivaldi.com/privacy/browser/) but it does not track or profile your browsing history, does not collect personally identifiable information, and does not sell your data to third parties. Google Chrome does all of these things. Vivaldi also offers built in protections to block trackers and ads while browsing. It is also a good idea to block Third-Party Cookies regardless of your choice of browser. 

# JavaScript

In order to further secure your data online consider using an extension like [NoScript](https://noscript.net/) to block sites from using JavaScript unless you grant them explicit permission to do so. This is a suggestion that I make primarily for more advanced users as it will “break” the majority of websites until you determine which scripts they require in order to function correctly. White-listing is always the preferred option over black-listing in any case (choosing the sites you allow to run scripts versus using an ad blocker to filter out ones that a third party has deemed malicious). Black-listing will cause your online persona to stand out more and often results in sites using even more aggressive options to track and profile you. Most people running ad-blockers have encountered the dreaded notification from sites asking them to politely turn off their ad-blocker in order to support the sites as content creators. What they are not being transparent about is the fact that in most cases they have already circumvented your ad-blocking software and employed even more malicious tactics to track and profile your browsing habits. To use a simplified analogy: it makes much more sense to give out your telephone number only to people you would like to be able to reach you than to give it to anyone who asks and to then have to spend all day blocking suspicious numbers. 

# Passwords

One of the most common breaches of data privacy in this day and age involves passwords and other login credentials. It is not uncommon for users to recycle easy to remember passwords and use them across multiple websites. This is especially troublesome when a site is breached as it may allow a malicious actor to access several or even all of your accounts across the Internet. Consider using a password manager such as [Bitwarden](https://bitwarden.com/) which allows you to randomly generate individual secure passwords for each website you visit. This means that when your credentials are inevitably exposed the malicious actor in question will only have access to the one site which was breached rather than also being able to log in to every other site for which you have reused the same password. Always enable two-factor authentication for sites containing any personal data but avoid using SMS as a second factor as it is easily intercepted and may even make it easier to access your login credentials. As an alternative I would suggest users employ the use of a secure second factor authentication app such as Aegis for Android or Authenticator for iOS. 

# Operating Systems

The next topic I would like to discuss is your choice of operating system. Android is probably the worst offender in this category because it is developed directly by Google and tied to their use of Play Services. Apple has a much better track record here with iOS but it is important to know which services to disable on any mobile platform in order to ensure your data is secure. Siri and other voice automation platforms are some of the worst offenders regarding data privacy and security. Consider disabling them altogether. I would also suggest checking the Privacy category under Settings on iOS and disabling anything and everything under that category including Location Services unless you are actively using an application which requires GPS functionality. Safari on iOS now includes built-in tracking protection which does a fairly decent job of blocking most cross-site tracking and includes a Privacy Report which allows you to view the results of said protections. As a general rule it is nearly always safer to use a mobile website versus the equivalent App Store / Play Store application. What you might lose in convenience and functionality you will gain in security and privacy. Social media applications such as Facebook and Instagram are particularly egregious regarding the amount of data they collect from users and the amount of tracking they perform. The iOS App Store includes an App Privacy section which allows you to view detailed information about the data apps collect, sell, and use to track you. Most users will likely gloss over this information but it is essential to take the time to read these privacy policies for every app you install in order to know what information you are providing and to whom. For advanced users who insist on sticking with the Android platform please consider [GrapheneOS](https://grapheneos.org/) as an alternative. GrapheneOS is a security hardened, de-Googled Android compatible platform with Google Play Services removed and primarily relies on the use of browser based solutions. 

Windows 10 is (perhaps surprisingly) one of the best options for data security and privacy as far as desktop operating systems are concerned providing one uses a local user account, disables Cortana, and toggles off everything under Settings > Privacy. For advanced users consider doing all browsing from within a hypervisor such as [Xen](https://xenproject.org) or [Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/), the latter of which is included with Windows 10. This will further protect your data in the event that your system becomes infected with spyware or other forms of malware. Desktop [Linux](https://madaidans-insecurities.github.io/linux.html) and [MacOS](https://hardware.substack.com/p/falling-out-of-love-with-apple-part1-5) currently sit in an abysmal state regarding security and privacy and I can therefore no longer recommend they be used unless from within a hypervisor. ChromeOS being Google software is also a rather poor option regarding data privacy unless Play Services are disabled and all browsing is done via the [Crostini](https://chromium.googlesource.com/chromiumos/docs/+/HEAD/containers_and_vms.md) virtual machine. 

# Conclusion

I hope this helps at least some of you to begin taking steps to ensure your online data remains private. Please reach out to me if you have any questions, comments, or suggestions regarding anything I have written about here.







