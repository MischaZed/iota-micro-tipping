# iota-micro-tipping
JavaScript library allowing to integrate IOTA micro tipping functionality with lowest possible efforts into any web application.

# IOTA Micro Tipping
JavaScript library allowing to integrate IOTA micro tipping functionality with lowest possible efforts into any web application.
  
## Application
1) After including this JavaScript Micro Tipping library in your HTML code, it will initialize itself in default mode. In default mode, no connection to the IOTA network will be established. Hence, only QR codes for micro tipping will be integrated.
2) If you want to connect to the IOTA network in order to query and display current tips, you need to initialize this JavaScript Micro Tipping library with a full node URL
   ```
    <script> 
        $(document).ready(function(){    
            $('[data-address]').microtipping("http://iota.bitfinex.com:80"); 
        });       
    </script>
    ```
3) Now that this JavaScript Micro Tipping library is integrated, you need to set markers and data where you want to display micro tipping QR codes, respectively, display current tips. Just apply the necessary data attribute "data-address" and the optional ones "data-tag" and "data-amount" to DOM objects that you want to transform into a micro tipping control
    > <span data-address="QPLGOG9PMIMUAW9UDMUNZQHPXZPXDNGLBEIHILXHWHIOFHLIHPDDERXAJQKUQDEORMHSUWVZQE9JYSHIWADIIPAOJD" data-tag="A Second Example" data-amount="10000"></span>
    
## Preparation
- [Download and] include JQuery library
    ```<script src="https://code.jquery.com/jquery-3.2.1.min.js" integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous"></script>```
- [Download and] include JQuery QRcode library
    ```<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery.qrcode/1.0/jquery.qrcode.min.js"></script>```
- Download and include IOTA JavaScript library (https://github.com/iotaledger/iota.lib.js/releases)
    ```<script src="js/iota.min.js"></script>```
- Download and include this IOTA Micro Tipping library
    ```<script src="js/iota-micro-tipping.js"></script>```
