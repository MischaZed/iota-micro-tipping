# IOTA Micro Tipping - A Simple JavaScript Plugin
JavaScript library allowing to integrate **IOTA micro tipping functionality** with **lowest possible efforts** into any web application. The goal of this micro tipping library is to make implementation as easy as possible in order to allow a wide adoption of IOTA for micro tiping purposes across the Internet. 

All you need to be able is to **(1)** integrate JavaScript libraries into your web site and **(2)** to apply HTML attributes to your HTML code. In the most simple scenario you would statically put them where you want a donation QR code to show up. In more dynamic web applications you could apply these via the template rendering engine dynamically below each relevant item. 

Imagine a web application that allows multiple users to register and write blog posts. You give these users an additional field in their user profile to set their donation address. Later, each time a user's blog post is rendered, the template rendering engine adds HTML attributes with the user's donation details, which is then transformed by this library into a micro tipping control field - with the option to display received tips.

<p align="center">
    <img src="https://i.imgur.com/Gc8se0o.png">
</p>
    
## Demo
A live sample can be found at https://noneymous.github.io/iota-micro-tipping/sample/sample.html 
If received donations are not loading, the chosen IOTA full node might be down.

## License and Donations
Feel free to use, change, enhance or share this JavaScript library for private or commercial use. Just don't sell/present it as your intellectual property. If this library was useful for you, please consider donating IOTAs: 
    
**```QPLGOG9PMIMUAW9UDMUNZQHPXZPXDNGLBEIHILXHWHIOFHLIHPDDERXAJQKUQDEORMHSUWVZQE9JYSHIWADIIPAOJD```**

## Important
The IOTA JavaScript library will not work in Internet Explorer. Hence, you cannot connect to the IOTA network using Internet Explorer in order to query donations. Nevertheless, Internet Explorer will still display donation QR codes generated by this library.

## Available Data Attributes
Available data attributes are:
- (Required) **data-address** The recipient address of the micro tip
- (Optional) **data-tag** A message to include in the transaction. This message will be used to divide tips for different items apart - If your library is set to connect to an IOTA full node and able to query transaction data.
- (Optional) **data-amount** You may suggest a default IOTA tip amount per item
        
<p align="right">
  <img src="https://i.imgur.com/kjtVhNQ.png">
</p>

## Customization
This IOTA micro tipping library comes with three functions ```initDom()```, ```updateQr()``` and ```updateTips()``` that can be adapted in order to tailor the micro tipping experience (DOM, CSS, JavaScript, user interaction,...) fitting your application.

## Initialization
1) After including this library in your HTML code, it will automatically initialize itself in default mode. No connection to the IOTA network will be established and only QR codes for receiving micro tips will be integrated.

2) Optionally, you can connect this library to an IOTA full node in order to query and display received tips.

    ```
    <script> 
         $(document).ready(function(){    
             $('[data-address]').microtipping("http://iota.bitfinex.com:80"); 
         });       
    </script>
    ```
    
2) This library will search your HTML code for DOM elements with relevant data attributes. You can use these data attributes to guide this library to DOM elements where you want to inject a micro tipping control. 

    ```
    <span data-address="QPLGOG9PMIMUAW9UDMUNZQHPXZPXDNGLBEIHILXHWHIOFHLIHPDDERXAJQKUQDEORMHSUWVZQE9JYSHIWADIIPAOJD" data-tag="A tag to associate a tip to an item" data-amount="10000"></span>
    ```
    
## Preparation
- [Download and] include JQuery library

    ```
    <script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
    ```

- [Download and] include JQuery QRcode library

    ```
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery.qrcode/1.0/jquery.qrcode.min.js"></script>
    ```
    
- Download and include IOTA JavaScript library (https://github.com/iotaledger/iota.lib.js/releases)

    ```
    <script src="js/iota.min.js"></script>
    ```
    
- Download and include this IOTA Micro Tipping library

    ```
    <script src="js/iota-micro-tipping.js"></script>
    ```
