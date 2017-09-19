# iota-micro-tipping
JavaScript library allowing to integrate IOTA micro tipping functionality with lowest possible efforts into any web application.

# IOTA Micro Tipping
JavaScript library allowing to integrate IOTA micro tipping functionality with lowest possible efforts into any web application.
  
## Initialization
1) After including this library in your HTML code, it will initialize itself in default mode automatically. In default mode, no connection to the IOTA network will be established. Hence, only QR codes for receiving micro tips will be integrated.

2) Optionally, you can connect this library to an IOTA full node in order to query and display received tips.

    ```
    <script> 
         $(document).ready(function(){    
             $('[data-address]').microtipping("http://iota.bitfinex.com:80"); 
         });       
    </script>
    ```
    
2) This library will search your HTML code for DOM elements with relevant data attributes. You can use these data attributes to guide this library to DOM elements where you want to inject a micro tipping control. Available data attributes are "data-address" and the optional "data-tag" and "data-amount" ones.
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
