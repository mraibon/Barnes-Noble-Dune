```python
# import libraries

from bs4 import BeautifulSoup
import requests
import smtplib
import time
import datetime
import csv
```


```python
# connect to Barnes and Noble

URL = 'https://www.barnesandnoble.com/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893'

headers = {"from my computer"}

page = requests.get(URL, headers=headers) # connecting my computer to the URL

# bring in the data

soup1 = BeautifulSoup(page.content, "html.parser")

# prettify (formats in a nice way)
soup2 = BeautifulSoup(soup1.prettify(), "html.parser")

print(soup2)
```

    <!-- Below forEach block added to generate redirectURL for productCategories, it's used in every PDP page -->
    <!-- 	Below block checks the value of lastLevelCategory i.e. leaf node with corresponding productCategory -->
    <!--  This if block is introduced to check if lastLevelCategory doesn't match productCategories' name though it's not empty hence setting first URL -->
    <!--  ATG-24700 -->
    <!-- ATG-25561 -->
    <!-- logic for meta description -->
    <!-- logic for title tag -->
    <!DOCTYPE html>
    
    <html class="no-js" lang="en">
    <head>
    <meta content="text/html; charset=utf-8" http-equiv="Content-Type"/>
    <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible"/>
    <meta content="True" name="HandheldFriendly"/>
    <meta content="320" name="MobileOptimized"/>
    <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
    <meta content="telephone=no" name="format-detection"/>
    <meta content="Barnes &amp; Noble" name="author"/>
    <title>
       Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune by Frank Herbert, Paperback | Barnes &amp; Noble®
      </title>
    <!-- set meta description -->
    <meta content="Perfect for longtime fans and new readers alike—a beautiful premium mass market boxed set of the first three novels in Frank Herbert's Dune" name="description"/>
    <meta content="summary" name="twitter:card"/>
    <meta content="@BNBuzz" name="twitter:site"/>
    <meta content="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune|Paperback" property="og:title"/>
    <meta content="Perfect for longtime fans and new readers alike&amp;mdash;a beautiful premium mass market boxed set of the first three novels in Frank Herbert's Dune Saga.In the far future, on a remote planet, an epic adventure awaits. Here are the first three novels of Frank Herbert&amp;rsquo;s..." property="og:description"/>
    <meta content="books.book" property="og:type"/>
    <meta content="https://www.barnesandnoble.com/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893" property="og:url">
    <meta content="http://prodimage.images-bn.com/pimages/9780593201893_p0_v3_s1200x630.jpg" property="og:image">
    <meta content="Barnes &amp; Noble" property="og:site_name">
    <link href="//img.images-bn.com/static/redesign/srcs/images/favicon.ico" rel="icon" type="image/x-icon"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/favicon.ico" rel="icon" sizes="16x16" type="image/x-icon"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/favicon.ico" rel="icon" sizes="32x32" type="image/x-icon"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/favicon.ico" rel="icon" sizes="24x24" type="image/x-icon"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/new-bn-icon-192x192.png" rel="icon" sizes="192x192"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-32.png" rel="icon" sizes="32x32"/>
    <!-- New cheat safari tab-->
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-192.png" rel="icon" sizes="96x96"/>
    <!-- New cheat for firefox -->
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon_96.png" rel="icon" sizes="48x48"/>
    <!-- New cheat for firefox -->
    <meta content="Barnes &amp; Noble" name="apple-mobile-web-app-title">
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-apple-touch-icon-180-any.png" rel="apple-touch-icon" sizes="any"/>
    <!--Legacy Apple -->
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-57.png" rel="apple-touch-icon" sizes="57x57"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-72.png" rel="apple-touch-icon" sizes="72x72"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-114.png" rel="apple-touch-icon" sizes="114x114"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-144.png" rel="apple-touch-icon" sizes="144x144"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-76.png" rel="apple-touch-icon" sizes="76x76"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-120.png" rel="apple-touch-icon" sizes="120x120"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-152.png" rel="apple-touch-icon" sizes="152x152"/>
    <link href="//img.images-bn.com/static/redesign/srcs/images/bn-icon-180.png" rel="apple-touch-icon" sizes="180x180"/>
    <!-- New Android -->
    <link href="/manifest.webmanifest" rel="manifest"/>
    <style>
             @-webkit-keyframes bugfix { from { padding: 0px; } to { padding: 0px; } }
    label span { -webkit-animation: bugfix infinite 1ms; }
            </style>
    <script async="" src="https://www.barnesandnoble.com/resources/a4c90d5ff473b1c6ba523607dbff42ea7ab0011ba05c2" type="text/javascript">
    </script>
    <script>
             window['adrum-start-time'] = new Date().getTime();
            </script>
    <!-- ATG-10336 Tactical fix starts -->
    <!-- change for ATG-18885 -->
    <link href="https://www.barnesandnoble.com/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577" rel="canonical"/>
    <!-- ATG-10336 Tactical fix starts -->
    <script async="" defer="" dvc="d" id="bcn" src="https://prod.accdab.net/cdn/cs/ebiaklm7tP0ykOyjm7KGfgNcPyo.js" type="text/javascript">
    </script>
    <script>
             var w=window;if(w.performance||w.mozPerformance||w.msPerformance||w.webkitPerformance){var d=document;AKSB=w.AKSB||{},AKSB.q=AKSB.q||[],AKSB.mark=AKSB.mark||function(e,_){AKSB.q.push(["mark",e,_||(new Date).getTime()])},AKSB.measure=AKSB.measure||function(e,_,t){AKSB.q.push(["measure",e,_,t||(new Date).getTime()])},AKSB.done=AKSB.done||function(e){AKSB.q.push(["done",e])},AKSB.mark("firstbyte",(new Date).getTime()),AKSB.prof={custid:"547626",ustr:"",originlat:"0",clientrtt:"208",ghostip:"23.219.171.5",ipv6:false,pct:"10",clientip:"73.115.155.43",requestid:"3e4dd5f9",region:"44095",protocol:"",blver:14,akM:"a",akN:"ae",akTT:"O",akTX:"1",akTI:"3e4dd5f9",ai:"238807",ra:"false",pmgn:"HTTP2Traffic",pmgi:"",pmp:"",qc:""},function(e){var _=d.createElement("script");_.async="async",_.src=e;var t=d.getElementsByTagName("script"),t=t[t.length-1];t.parentNode.insertBefore(_,t)}(("https:"===d.location.protocol?"https:":"http:")+"//ds-aksb-a.akamaihd.net/aksb.min.js")}
            </script>
    <script>
             bazadebezolkohpepadr="2095866202"
            </script>
    <script defer="" src="https://www.barnesandnoble.com/akam/13/7cec613e" type="text/javascript">
    </script>
    </meta>
    </meta>
    </meta>
    </meta>
    </head>
    <body class="pdpPage bncom-responsive" data-global-svg-assets-url="/static/redesign/srcs/images/global-assets.svg">
    <span hidden="" id="enableADI">
       true
      </span>
    <span hidden="" id="adiJSUrl">
       https://prod.accdab.net/cdn/cs/ebiaklm7tP0ykOyjm7KGfgNcPyo.js
      </span>
    <span hidden="" id="adiJSTimeout">
       500
      </span>
    <img alt="BN Homepage Two-Image carousal" height="99999" src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48c3ZnIHdpZHRoPSI5OTk5OXB4IiBoZWlnaHQ9Ijk5OTk5cHgiIHZpZXdCb3g9IjAgMCA5OTk5OSA5OTk5OSIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIj48ZyBzdHJva2U9Im5vbmUiIGZpbGw9Im5vbmUiIGZpbGwtb3BhY2l0eT0iMCI+PHJlY3QgeD0iMCIgeT0iMCIgd2lkdGg9Ijk5OTk5IiBoZWlnaHQ9Ijk5OTk5Ij48L3JlY3Q+IDwvZz4gPC9zdmc+" style="pointer-events: none; position: absolute; top: 0; left: 0; width: 99vw; height: 99vh; max-width: 99vw; max-height: 99vh;" width="99999"/>
    <link href="//css.css-bn.com/static/redesign/release/css/toolkit-bootstrap.min.css?v11.4.4&amp;setviewtype=full" rel="stylesheet" type="text/css"/>
    <link href="//css.css-bn.com/static/redesign/release/css/bn-responsive-wb.min.css?v11.4.4&amp;setviewtype=full" media="print" onload="this.media='all'" rel="stylesheet"/>
    <link href="" media="print" onload="this.media='all'" rel="stylesheet" type="text/css"/>
    <script>
          if (performance.mark === undefined) {
    console.log("performance.mark not supported");
    }else{
    performance.mark("Above_the_fold_loading_starts");
    }
    if(typeof performance.measure === 'undefined')
    {
    console.log("Create Measures: performance.measure not supported");
    }
    
    function getCookieBn(cname) {
    let name = cname + "=";
    let decodedCookie = decodeURIComponent(document.cookie);
    let ca = decodedCookie.split(';');
    for(let i = 0; i <ca.length; i++) {
    let c = ca[i];
    while (c.charAt(0) == ' ') {
    c = c.substring(1);
    }
    if (c.indexOf(name) == 0) {
    return c.substring(name.length, c.length);
    }
    }
    return "";
    }
    function readOneTrustCookie (param) {
    var OptanonConsentCookie = getCookieBn('OptanonConsent');
    var queryParams = new URLSearchParams(OptanonConsentCookie);
    var cookieGroups = queryParams.get('groups');
    var cookieObject = eval('({' + cookieGroups + '})');
    return cookieObject[param];
    }
    function addScriptBn( src,param2 ) {
    var s = document.createElement( 'script' );
    s.setAttribute( 'src', src );
    if (param2=== 'async') {
    s.setAttribute( 'param2', true );
    }
    document.body.appendChild( s );
    }
         </script>
    <script>
          if(typeof performance.mark !== 'undefined')
    {
    /* ATG-24315 Fix start */
    var bodyClass = 'pdpPage';
    var indexOfPDPPageClass = bodyClass.indexOf('pdpPage');
    if( indexOfPDPPageClass > -1){
    /* ATG-24315 Fix end */
    performance.mark('Cover_Image/Video_loading_starts');
    performance.mark("Addtocart_loading_starts");
    }
    performance.mark("Global_Header_loading_starts");
    }
         </script>
    <script>
          if(typeof performance.mark !== 'undefined' && typeof performance.measure !== 'undefined')
    {
    performance.mark("Global_Header_loading_ends");
    performance.measure(
    "globalHeaderDur",
    "Global_Header_loading_starts",
    "Global_Header_loading_ends"
    );
    }
         </script>
    <div class="browser-notice ie-outdated hidden">
    <div>
    <span class="x">
            ×
           </span>
    <p>
    <strong>
             Uh-oh, it looks like your Internet Explorer is out of date.
            </strong>
    <br/>
    <br/>
            For a better shopping experience, please
            <a href="http://windows.microsoft.com/en-us/internet-explorer/download-ie/" target="_blank">
             upgrade now.
            </a>
    </p>
    </div>
    </div>
    <script>
          // migration changes SRL-92
    /*  if($.browser.msie && parseInt($.browser.version, 10) <=10){
    if(!$('.ie-outdated').is('visible')){
    $('.ie-outdated').show();
    }
    }    */
    if (navigator.userAgent.indexOf('MSIE') != -1)
    var detectIEregexp = /MSIE (\d+\.\d+);/ //test for MSIE x.x
    else // if no "MSIE" string in userAgent
    var detectIEregexp = /Trident.*rv[ :]*(\d+\.\d+)/ //test for rv:x.x or rv x.x where Trident string exists
    if(detectIEregexp.test(navigator.userAgent)){ //if some form of IE
    var ieversion=new Number(RegExp.$1) // capture x.x portion and store as a number
    if (ieversion<=10){
    if(!$('.ie-outdated').is('visible')){
    $('.ie-outdated').show();
    }
    }
    }
    // migration changes end SRL-92
         </script>
    <noscript>
    <div class="browser-notice">
    <div>
    <p class="circle">
             !
            </p>
    <p>
             Javascript is not enabled in your browser. Enabling JavaScript in your browser will allow you to experience all the features of our site.
             <a href="https://help.barnesandnoble.com">
              Learn how to enable JavaScript on your browser
             </a>
    </p>
    </div>
    </div>
    </noscript>
    <input id="deferAdLoad" type="hidden" value=""/>
    <input name="imagePath" type="hidden" value="/static/redesign/srcs/images/"/>
    <input name="spinnerPath" type="hidden" value="//img.images-bn.com/static/redesign/srcs/images/spinner.svg"/>
    <script>
          var SITE_PROTOCOL = document.location.protocol||window.location.protocol||'http:',
    SITE_DOMAIN = document.location.hostname||window.location.hostname||'www.barnesandnoble.com',
    SITE_PORT = document.location.port||window.location.port||'80',
    THIS_PATH = document.location.pathname||window.location.pathname||'/cartridges/ProductPageSlot/ProductPageSlot.jsp',
    SITE_DOMAIN_URL = THIS_PAGE = SITE_ROOT = port = "",
    STATIC_ASSETS_PATH = "/static",
    webContextRoot ='',
    staticAssetVersion = '?v11.4.4',
    XHR_FOLDER ='/xhr',
    XHR_HANDLER_PATH = XHR_FOLDER+'/handler.jsp',
    PAGE_DEBUG_MODE = false;
    // indexExchngHeaderBiddingJsUrl="";
    // enableIndexExchangeJS="";
    if(SITE_PROTOCOL=="https:") {
    XHR_FOLDER = '/xhr';
    XHR_HANDLER_PATH = XHR_FOLDER+'/handler.jsp';
    }
    if(SITE_PORT.length > 0 && SITE_PORT!=80)
    port = ":"+SITE_PORT;
    SITE_DOMAIN_URL = SITE_PROTOCOL + "//" + SITE_DOMAIN + port;
    SITE_ROOT = SITE_DOMAIN_URL + webContextRoot;
    THIS_PAGE = SITE_DOMAIN_URL + THIS_PATH;
    port = null;
    function consoleLog() {
    if (PAGE_DEBUG_MODE!==true) return;
    if (typeof console != "undefined" && typeof console.log != "undefined") {
    if (typeof console.log.apply != "undefined") {
    console.log.apply(console,arguments);
    } else {
    for(var i=0;i<arguments.length;i++) {
    var arg = arguments[i];
    console.log(arg);
    }
    }
    }
    }
    function consoleWarn() {
    if (PAGE_DEBUG_MODE!==true) return;
    if (typeof console == "undefined") return;
    if (typeof console.warn != "undefined" && typeof console.warn.apply != "undefined") {
    console.warn.apply(console,arguments);
    } else {
    consoleLog.apply(console,arguments);
    }
    }
    function consoleError() {
    if (PAGE_DEBUG_MODE!==true) return;
    if (typeof console == "undefined") return;
    if (typeof console.error != "undefined" && typeof console.error.apply != "undefined") {
    console.error.apply(console,arguments);
    } else {
    consoleWarn.apply(console,arguments);
    }
    }
    var captchaV3Enabled = 'true';
    
    function addOnLoadEvent(func) {
    var oldonload = window.onload;
    var newonload = function(){
    /* if(enableIndexExchangeJS ==="true" && indexExchngHeaderBiddingJsUrl !=="" ){
    // ATG-24008 : Add header bidding management from IndexExchange
    headerBiddingJS();
    }  */
    func();
    };
    if (typeof window.onload != 'function') {
    window.onload = newonload;
    } else {
    window.onload = function() {
    if (oldonload) {
    oldonload();
    }
    newonload();
    }
    }
    }
         </script>
    <!-- migration changes SLR-92 -->
    <script>
          document.write("<script type='text/javascript' src='//js.js-bn.com/static/redesign/release/js/head.js?v11.4.4'><\/script>");
         </script>
    <!--// migration changes SLR-92 -->
    <script>
          function updateMiniCartCount(count) {
    if(typeof count != 'undefined' && count != $.trim($('.bagTotal').text())) {
    $('.bagTotal').text(count);
    }
    }
    function miniCartEvents($container) {
    var spinnerSrc = "",
    spinnerImgPath = $('input[name=spinnerPath]').val();
    if(spinnerImgPath && spinnerImgPath.indexOf('null') < 0 && spinnerImgPath.indexOf('undefined') < 0 ){
    spinnerSrc = spinnerImgPath;
    }
    var $spinner = $('<div class="spinner spinner__large"><img tabindex="0" src="' + spinnerSrc + '" role="presentation" aria-live="polite" aria-label="Laoding..."></div>').addClass('mini-cart-spinner'),
    $quantityUpdateForms = $('.mini-cart-quantity-update');
    BN.MiniCart = new MiniCart('#miniCart', '#shoppingBag');
    // shopping bag flyout only
    $('#bagContentsContainer').find('.mini-cart-quantity-update').each(function() {
    BN.uXHR.Form.apply(this);
    });
    $quantityUpdateForms.find('.product-quantity').each(function() {
    var $this = $(this);
    $this.data('initial-value', $this.val());
    });
    $quantityUpdateForms.find('input[type=submit]').on('click', function(e) {
    var $theForm = $(this).closest('form'),
    $eleProductQuantity = $theForm.find('.product-quantity').first(),
    productQuantity = $eleProductQuantity.length ? $eleProductQuantity.val().trim() : '';
    if (productQuantity.length == 0) {
    e.preventDefault();
    /* reset to the initial quantity if the user tried to submit an empty value */
    if ($eleProductQuantity.length && $eleProductQuantity.data('initial-value')) {
    $eleProductQuantity.val($eleProductQuantity.data('initial-value'));
    }
    }
    });
    $quantityUpdateForms.on('submit', function() {
    var $this = $(this),
    $miniCartItem = $this.parents('#miniCart');
    $spinner.appendTo($miniCartItem);
    }).on('amplifiFormSuccess', function(e, response) {
    //Adobe Analytics: updates cart object
    if(typeof s_setP !== 'undefined') updateAnalyticsCart();
    // check to shopping bag reload flag is on page
    // if shopping bag is updated in dropdown and page
    // contains the items, it must be refreshed
    if ($("#shoppingBagReloadFlag").length){
    consoleLog("Reload Page to update shopping bag.");
    location.reload(true);
    } else {
    $('#miniCartItems .miniCartItems-list').load(webContextRoot+"/checkout/includes/get-mini-cart-commerce-items.jsp", miniCartEvents);
    $('#subtotalLine .subtotal-amount').html('$'+response.data.subtotal);
    $('#subtotalLine .item-count').html('('+response.data.totalQuantity+' items)');
    $('.bagTotal').html(response.data.totalQuantity);
    if(response.data.totalQuantity < 1) {
    //DONT SHOW CART IF TYPE AHEAD IS OPEN
    if($('#headSearchTypeAheadHolder').is(':visible')) {
    loadHeaderElement($("#bagContentsContainer"), webContextRoot+"/includes/shopping-bag.jsp", true, true);
    } else {
    loadHeaderElement($("#bagContentsContainer"), webContextRoot+"/includes/shopping-bag.jsp", true, false);
    }
    }
    }
    $spinner.remove();
    if(e.target.id && /remove/i.test(e.target.id) || $(this).data('form-type') === 'remove') {
    $(this).trigger('analytics-mini-cart-remove');
    } else {
    $(this).trigger('analytics-mini-cart-add');
    }
    }).on('amplifiFormError', function(e, response) {
    $spinner.remove();
    });
    }
    function loadHeaderElement($container, frag, miniCartLoaded, hideCart) {
    $.ajax({
    url: frag,
    cache: false,
    type: "get",
    beforeSend: function() {
    if(!$('#miniCart').length) {
    }
    }
    }).done(function(data) {
    $container.html(data);
    if (hideCart) {
    $("#miniCart").css("display", "none");
    }
    if (miniCartLoaded) {
    updateMiniCartCount($('#miniCartQuantityVal').val());
    miniCartEvents();
    }
    //to update the mini cart count after redesign
    $('.cart-slide-out__banner').find('.bagTotal').html($('#bagTotal').html());
    if($('body').hasClass('landingPage') || $('body').hasClass('shopping-bag') || $('body').hasClass('homepage')){
    $('#checkoutFormSB .sign-in-checkout').attr('data-params','{"tplParams":{"isCheckout":"true","isNew":"true"}}');
    }
    /*                 //to bind the spinner functionality
    $('[data-trigger="spinner"]').spinner('delay', 0).spinner('changed', function (e) {
    $(e.target).trigger('change');
    }); */
    });
    }
    function displayHeaderFooterData(dataObj) {
    try {
    if(typeof dataObj != 'undefined' && dataObj != '') {
    //set login status variables
    if(typeof BN != 'undefined') {
    BN.isExplicitlyLoggedIn = dataObj.isSecureLogin;
    BN.isSoftLoggedIn = dataObj.isSoftLoggedIn;
    } else {
    $(document).ready(function() {
    BN.isExplicitlyLoggedIn = dataObj.isSecureLogin;
    BN.isSoftLoggedIn = dataObj.isSoftLoggedIn;
    });
    }
    //populate sign in/account links data
    //$('#authBar').html(dataObj.signInHtml);
    if($('.account-links').find('#signInLink').length > 0){
    $('#signInLink').remove();
    }
    if($('.account-links').find('.account-sign-in').length > 0){
    $('.account-sign-in').remove();
    }
    $('.account-links').prepend(dataObj.signInHtml);
    $('#myAccountMenu').html(dataObj.accountLinksHtml);
    if(dataObj.isSecureLogin === true){
    $('.account-links').attr('data-user-state','signed-in');
    }
    $(document).on('click', '#myAccountMenu #myAccountLink', function(){
    $(this).addClass('focus');
    });
    updateMiniCartCount(dataObj.cartQuantity);
    HEADERLOADED = true;
    HEADERDATA = '';
    bnLoggingEnabled = dataObj.bnLoggingEnabled;
    $("#myAccountMenu").click(function(e) {
    if($(e.target).attr('id') == 'myAccountLink')
    e.preventDefault();
    $("#myAccountLinks").toggleClass("showMyAccountLinks");
    });
    }
    } catch(err) {
    console.log(err);
    }
    }
    function loadEmailSignUp() {
    // check for email signup class in CQ template
    if ($(".global-footer-email-signup").length){
    // bind form to framework
    var $form = $('#emailSignupForm');
    BN.Validate.Listen($form);
    BN.uXHR.Form.apply($form);
    // success action
    $('#emailSignupForm').on('amplifiFormSuccess', function() {
    $('#emailSignupDiv').html("<span>Thank you for submitting your email address.</span>");
    $('.global-footer-email-signup').find('.mini-cart-spinner').remove();
    }).on("amplifiFormBeforeSerialize", function(){
    $('#emailSignupForm').find('.handler-email-signup').remove();
    $('#emailSignupForm').append('<input class="handler-email-signup" type="hidden" name="amplifiHandler" value="/atg/userprofiling/ProfileFormHandler.emailSignup">');
    }).on("amplifiFormError",function(event,err,xhr,status,msgs){
    var errors = msgs.items;
    BN.Validate.DisplayErrors(this, errors);
    $form.find('input[type=text]').addClass('user-error');
    $('.global-footer-email-signup').find('.mini-cart-spinner').remove();
    }).on("amplifiFormBeforeSubmit",function(){
    consoleLog("Calling displaySpinner");
    $form.find('input[type=text]').removeClass('user-error');
    $('.global-footer-email-signup').append($('<div/>').addClass('mini-cart-spinner'));
    });
    }
    }
    /* ATG-10818: Pre-populate footer email field only when user is logged in */
    function populateEmailSignUp(data) {
    $(document).ready(function() {
    if(data.isSecureLogin){
    $('#emailAddr').val(data.email);
    }
    });
    }
    //load header elements for akamai caching
    //SIGN IN Links, PTA Link, EMAIL SIGN UP, CART DETAILS
    function loadDynamicHeaderElements(callback) {
    $.ajax({
    url: '/xhr/header-footer-data.jsp',
    cache: false,
    type: "get",
    dataType: 'json'
    }).done(function(data) {
    HEADERDATA = data;
    HEADERLOADED = false;
    if($('#userLinks').length) {
    displayHeaderFooterData(HEADERDATA);
    } else {
    $(document).ready(function() {
    displayHeaderFooterData(HEADERDATA);
    });
    }
    populateEmailSignUp(data);
    });
    $(document).ready(function() {
    loadEmailSignUp();
    //miniCartEvents();
    });
    }
         </script>
    <script>
          loadDynamicHeaderElements();
         </script>
    <!-- ATG-25918 -->
    <script src="//assets.adobedtm.com/d55bc227c346/0aaa96eebcd0/launch-d923d12e2af4.min.js">
    </script>
    <!-- ATG-26292 -->
    <script>
          $(document).ready(function(){
    window.addEventListener("OneTrustGroupsUpdated",event =>{
    var oneTrustCookiePerformance = readOneTrustCookie('C0003');
    if (oneTrustCookiePerformance === 1) {
    addScriptBn('https://apps.bazaarvoice.com/deployments/barnesandnoble/local_implementation/production/en_US/bv.js','async');
    }
    });
    var oneTrustCookiePerformance = readOneTrustCookie('C0003');
    if (oneTrustCookiePerformance === 1) {
    addScriptBn('https://apps.bazaarvoice.com/deployments/barnesandnoble/local_implementation/production/en_US/bv.js','async');
    }
    });
         </script>
    <script>
          var enableGoogleAdsAfterPageLoad = true;
         </script>
    <script>
          var asyncRelatedAdsEnabled = true;
         </script>
    <script type="text/javascript">
          /*$(document).ready(function() {
    $('#primaryNav').on('hover touchstart', function() {
    $('.nav-menu').css('display', 'block');
    });
    $('#primaryNav li.nav-item a').on('focus', function() {
    $('.nav-menu').css('display', 'block');
    });
    });*/
    function set_cookie (cvalue) {
    
    var cname = "internalCampaign";
    cvalue = cvalue.replace(/ /gi,'-').replace(/[`~!@#^&*()|+\=ï¿½ï¿½?;:'",<>\{\}\[\]\\\/]/gi, '').toLowerCase()
    cvalue = 'pdp_' +  cvalue;
    //cvalue = encodeURI(cvalue);
    var d = new Date();
    d.setTime(d.getTime() + (1*24*60*60*1000));
    var curCookie = cname + "=" + cvalue +
    "; expires=" + d.toGMTString() +
    "; path=" + "/"  +
    "; domain=" + SITE_DOMAIN;
    document.cookie = curCookie;
    
    }
    // ATG-24008 : Add header bidding management from IndexExchange
    /*  function headerBiddingJS(){
    var indxexctag=document.createElement("script");
    indxexctag.type = "text/javascript";
    indxexctag.async=true;
    indxexctag.src = indexExchngHeaderBiddingJsUrl;
    var node = document.getElementsByTagName("head")[0];
    node.appendChild(indxexctag);
    } */
         </script>
    <script async="" src="//js.js-bn.com/static/redesign/srcs/js/vendor/com.liquidpixels.Resolve.js?v11.4.4" type="text/javascript">
    </script>
    <script crossorigin="" src="https://www.barnesandnoble.com/static/redesign/srcs/js/react.production.min.js">
    </script>
    <script crossorigin="" src="https://www.barnesandnoble.com/static/redesign/srcs/js/react-dom.production.min.js">
    </script>
    <script>
          document.write("<script type='text/javascript' src='//js.js-bn.com/static/redesign/release/js/commerce-header.js?v11.4.4'><\/script>");
         </script>
    <script defer="" src="https://www.google.com/recaptcha/api.js?render=6LdspeQUAAAAADObEWJ6oo7G-QvgkhiLgMgDXn_v">
    </script>
    <script>
          var captchaV3ApiKey= '6LdspeQUAAAAADObEWJ6oo7G-QvgkhiLgMgDXn_v';
         </script>
    <div id="header">
    </div>
    <script type="text/javascript">
          /*CommerceHeaderFooter is the name of the library that we defined in webpack.config.js */
    CommerceHeaderFooter.showHeader('header', {env:'prod', consumer_host:'https://www.barnesandnoble.com', styling:'responsive'});
         </script>
    <div id="screen">
    </div>
    <main class="invisible bg-whole-site-color" role="main">
    <div class="gnb">
    <style type="text/css">
            .homepage .tile-grid {margin:3px 0 0 0; padding:0; } #globalNavBanner {margin: 0 auto 0; padding-bottom:4px; } #globalNavBanner.image { padding-bottom:3px; } .globalNavBanner{width:100%;max-width: 100%;text-align: center;} .globalNavBannerLink {display:block;text-decoration: none; border:1px solid transparent; line-height: 0;border-left: 0;border-right:0;margin:0 auto; width: 100%;} .globalNavBannerLink:hover,.globalNavBannerLink:focus{border-color:#7c83bc;text-decoration: none;} a.globalNavBannerLink.nolink{cursor:default;} .globalNavBanner img { width: 100%;} @media screen and (min-width:601px) and (max-width:899px){ .globalNavBanner img { max-width: 120%; width: 120%; position: relative; left: -10%;} } #globalNavBanner:not(.image) .gsb-table{display:table;min-height: 66px;width: 100%;max-width:1440px;margin: 0 auto;} .globalNavBanner .gsb-row{display:table-row} .globalNavBanner .gsb-td{display:table-cell;vertical-align:middle; } .globalNavBanner .gsb-message{ color:#000000;font-family:Lato,serif;font-size:18px; line-height:1.45; letter-spacing: 0.56px;font-weight:600; padding:7px 16%; position:relative} .globalNavBanner .gsb-code-phrase {font-weight: normal; border-left:solid 1px #979797; padding-left:14px; margin-left:9px; line-height:1.45; } .globalNavBanner .gsb-code { font-size: 16px; line-height:1.45; font-weight: bold; letter-spacing: 0.57px; } .globalNavBanner .gsb-cta{ font-family:Lato;font-size:16px;font-weight:normal; line-height: 1.2; letter-spacing:0.12px;color:#000000; display:inline-block;width:fit-content;text-align:center;padding:0;border-bottom:1px #000000 solid; position:absolute;right:30px; margin-top: 2px; } @media screen and (max-width:949px){ .globalNavBanner .gsb-message{font-size:16px; line-height:1.45; letter-spacing:0.57px} .globalNavBanner .gsb-code-phrase { font-size: 16px; letter-spacing: 0.57px;} .globalNavBanner .gsb-code { font-size: 14px; font-weight: bold; letter-spacing: 0.5px; } .globalNavBanner .gsb-cta{font-size:14px; letter-spacing:0.11px;width:fit-content; bottom:6px;} } @media screen and (max-width:850px){ .globalNavBanner .gsb-code-phrase { border-left-width:0; padding-left: 0; margin-left: 0; display: block; } } @media screen and (max-width:775px){ .globalNavBanner .gsb-message{font-size:15px; line-height:1.35; } .globalNavBanner .gsb-code-phrase {font-size: 15px;line-height:1.35; letter-spacing: 0.09px;} .globalNavBanner .gsb-code { font-size: 15px; line-height:1.35; font-weight: bold; } .globalNavBanner .gsb-cta{font-size:13px; } } @media screen and (max-width:600px){ .globalNavBanner .gsb-message{font-size:14px; line-height:1.35;letter-spacing: 0.11px; padding:10px 5%; } .globalNavBanner .gsb-code-phrase { font-size: 12px;line-height:1.35; letter-spacing: 0.09px;} .globalNavBanner .gsb-code { font-size: 12px; font-weight: bold;line-height:1.35; } .globalNavBanner .gsb-cta{font-size:12px; letter-spacing: 0.09px; } #globalNavBanner:not(.image) .gsb-table, #globalNavBanner.noncpn .gsb-table{display:table;min-height:42px; ;} #globalNavBanner.noncpn .globalNavBanner .gsb-cta{ position: static; bottom: unset; right: unset; font-size: 14px; line-height: 1.35; letter-spacing: 0.11px; margin-left: 8px; } } @media screen and (min-width:992px) and (max-width:1023px){ .globalNavBanner .gsb-cta{right:22px;} } @media screen and (min-width:601px) and (max-width:991px){ .globalNavBanner .gsb-cta{right:16px;} } @media screen and (max-width:600px){ .globalNavBanner .gsb-cta{right:12px;} } @media screen and (max-width:350px){ .globalNavBanner .gsb-message{line-height:1.25; } .globalNavBanner .gsb-code-phrase { line-height:1.25; } .globalNavBanner .gsb-code {line-height:1.25; } .globalNavBanner .gsb-cta{bottom: 4px;} }
           </style>
    <style type="text/css">
            .globalBannerWrap{background-color: #C0E1F4;} #globalNavBanner.image .globalBannerWrap{background-color:transparent !important;} #globalNavBanner.image .globalBannerWrap.primary {background-image:none;} #globalNavBanner.image .globalBannerWrap.secondary {background-image:none;}
           </style>
    <div id="globalNavBanner">
    <div class="globalNavBanner hidden globalBannerWrap">
    <a class="globalNavBannerLink">
    </a>
    </div>
    <script type="text/javascript">
             (function(){
    
    var secondBanner = false;
    var thisPathName = window.location.pathname;
    $(".globalNavBanner:not(.loaded)").each(function(index){
    
    if(thisPathName !== "/h/help/about/terms-of-use" && thisPathName !== "/h/copyright-policy") {
    
    if(109 > 1){
    $('a.globalNavBannerLink').attr('href','https://www.barnesandnoble.com/b/books/kids-book-awards/barnes-noble-childrens-ya-book-awards/_/N-29Z8q8Z2ve8');
    }else{
    $('a.globalNavBannerLink').addClass('nolink');
    }
    if( 109 > 1 && "same" === "modal" ){
    $('a.globalNavBannerLink').attr('target', '_blank').attr('data-modal-class', 'BN.Modal.External.Link').attr('data-modal-scrolling', 'yes').attr('data-modal-title', '');
    }else if ( 109 > 1 && "same" === "new" ){
    $('a.globalNavBannerLink').attr('target', '_blank');
    }
    $(this).addClass('primary loaded').parents('#globalNavBanner').addClass("noncpn image");
    var msgElem;
    
    
    msgElem = `<picture><source media="(max-width: 600px)" srcset="//dispatch.barnesandnoble.com/content/dam/ccr/global/global-nav-banner/2024/03/PROD-28971-GlobalNav_ChildrensYABookAwards_3-27-Mobile.jpg"><source media="(min-width: 601px)" srcset="//dispatch.barnesandnoble.com/content/dam/ccr/global/global-nav-banner/2024/03/PROD-28971-GlobalNav_ChildrensYABookAwards_3-27-Desktop.jpg"><img src="//dispatch.barnesandnoble.com/content/dam/ccr/global/global-nav-banner/2024/03/PROD-28971-GlobalNav_ChildrensYABookAwards_3-27-Desktop.jpg" class="globalNavBannerImg" alt="Just Announced The Barnes &amp; Noble Children&#039;s &amp; YA Book Awards Shortlists.  Explore Now "></picture>`;
    
    
    
    $('a.globalNavBannerLink').html(msgElem);
    $("a.globalNavBanner").on("click", function(){
    set_cookie("globalNavBanner_just-announced-the-barnes--noble-childrens--ya-book-awards-shortlists.--explore-now_na_text");
    });
    $(this).removeClass('hidden');
    
    } else if(secondBanner && (thisPathName === "/h/help/about/terms-of-use" || thisPathName === "/h/copyright-policy")) {
    
    if(0 > 1){
    $('a.globalNavBannerLink').attr('href','');
    }else{
    $('a.globalNavBannerLink').addClass('nolink');
    }
    if( 0 > 1 && "same" === "modal" ){
    $('a.globalNavBannerLink').attr('target', '_blank').attr('data-modal-class', 'BN.Modal.External.Link').attr('data-modal-scrolling', 'yes').attr('data-modal-title', '');
    }else if ( 0 > 1 && "same" === "new" ){
    $('a.globalNavBannerLink').attr('target', '_blank');
    }
    $(this).addClass('secondary loaded').parents('#globalNavBanner').addClass("noncpn  ");
    var msgElem2;
    
    
    
    msgElem2 = `<div class="gsb-table"> <div class="gsb-row"> <div class="gsb-message gsb-td">    <div class="gsb-cta  gsb-tdd"></div> </div> </div></div>`;
    
    
    $('a.globalNavBannerLink').html(msgElem2);
    $("a.globalNavBanner").on("click", function(){
    set_cookie("globalNavBanner__na_text");
    });
    $(this).removeClass('hidden');
    
    } else {
    $( ".cqGlobalNavBanner" ).hide();
    };
    
    });
    }());
    $(function() {
    if (window.location.href.indexOf("barnesandnoble.com/w/") > -1){
    var pCategory = digitalData.product[0].category.primaryCategory.replace(/[^a-z0-9\s]/gi, '').replace(/[_\s]/g, '-').toLowerCase();
    if (pCategory.length > 0){
    sessionStorage.setItem('optPrimaryCategory', pCategory);
    sessionStorage.setItem('optDDprimaryCategory', pCategory);
    }else{
    sessionStorage.setItem('optPrimaryCategory', 'none');
    sessionStorage.setItem('optDDprimaryCategory', 'none');
    }
    var optDDproductType = digitalData.product[0].category.productType.replace(/[^a-z0-9\s]/gi, '').replace(/[_\s]/g, '-').toLowerCase();
    if (optDDproductType.length > 0){
    sessionStorage.setItem('optDDproductType', optDDproductType);
    }else{
    sessionStorage.setItem('optDDproductType', 'none');
    }
    }
    });
            </script>
    </div>
    <div class="globalSubBanner" id="globalSubBanner">
    <style type="text/css">
             .globalSubBanner{margin:0 auto 4px;} .globalSubWrap{width:100%;text-align:center;background:#3d5962;margin:0;} .globalSubBanner .gsb-table{display: table; width: 100%;min-height:42px;max-width:1440px;margin: 0 auto;} .globalSubBanner .gsb-row{display:table-row} .globalSubBanner .gsb-td{display:table-cell;vertical-align:middle} .globalSubBannerlink {width:100%; display:block;text-decoration: none; border:1px solid transparent; border-left: 0;border-right:0; line-height: 0;} .globalSubBannerlink:hover,.globalSubBannerlink:focus{border-color: #89CFF0 ; text-decoration: none;} .globalSubBanner .gsb-message{color:#f6f3f3;font-family:Lato,serif;font-size:16px;font-weight:600;line-height:1.13;letter-spacing:.53px; padding:10px 6%; position:relative; } .globalSubBanner .gsb-cta{font-family:Lato;font-size:16px;font-weight:600; line-height:1.36;letter-spacing:0.53px;color:#f6f3f3;display:inline-block;width:fit-content;text-align:center;padding:0;border-bottom:1px #fff solid;position:absolute;right:22px;} .globalSubBanner .gsb-link {color:#f6f3f3; display: inline-block;text-decoration: underline;padding-left: 8px;} @media screen and (max-width:949px){ .globalSubBanner .gsb-message{font-size:14px;line-height:normal;letter-spacing:.47px} .globalSubBanner .gsb-cta{font-size:14px;width:fit-content}} @media screen and (max-width:600px){ .globalSubBanner .gsb-message{font-size:14px;} .globalSubBanner .gsb-cta{font-size:12px;letter-spacing: 0.09px;} } @media screen and (max-width:375px){ .globalSubBanner .gsb-message{font-size:13px;} .globalSubBanner .gsb-cta{font-size:12px} }
            </style>
    <div class="globalSubWrap">
    <a class="globalSubBannerlink" href="https://www.barnesandnoble.com/membership/" onclick="set_cookie('globalSubBanner_premium-members-get-10-off-and-earn-rewards_na_text');">
    <div class="gsb-table">
    <div class="gsb-row">
    <div class="gsb-message gsb-td">
                 Premium Members Get 10% Off and Earn Rewards
                 <span class="gsb-link">
                  Find Out More
                 </span>
    </div>
    </div>
    </div>
    </a>
    </div>
    </div>
    </div>
    <div class="pdp-container bg-whole-site-color bn-badge-added-pdp bn-book-size pdp pdp-books" id="pdp-page-container" itemprop="mainEntity" itemscope="" itemtype="http://schema.org/Product">
    <div class="hidden" itemprop="aggregateRating" itemscope="" itemtype="http://schema.org/AggregateRating">
    <span class="rating-value" itemprop="ratingValue">
    </span>
    <span class="rating-count" itemprop="reviewCount">
    </span>
    <span itemprop="bestRating">
             5
            </span>
    <span itemprop="worstRating">
             1
            </span>
    </div>
    <link href="https://schema.org/Book" itemprop="additionalType"/>
    <!-- ATG-19085 fix starts -->
    <input id="isAdultContent" type="hidden" value="false"/>
    <!-- ATG-19085 fix ends -->
    <div class="PageContent" id="hero-section-placeholder">
    <!-- ATG-24840 Audiobook rebranding -->
    <input id="isBopisEnabled" type="hidden" value="true"/>
    <input id="pdpBopisSecLazyLoad" type="hidden" value="false"/>
    <input id="isCommerceHub" type="hidden" value="false"/>
    <!-- ATG-24840 -->
    <!-- ATG-24840 END-->
    <aside class="error-msg alert alert--error mt-xs" id="pdpErrors" role="alert" style="display:none;">
    </aside>
    <section id="hero-section">
    <input id="breadCrumbsText" name="breadCrumbsText" type="hidden" value="Books"/>
    <div class="pdp-base-container pt-0 pb-ss text--left nav-section" id="pdp-header-container">
    <nav class="breadCrumbNav invisible" data-nav="mainNav" role="navigation">
    <ol class="lists lists--unstyled lists--bread-crumbs" itemscope="" itemtype="http://schema.org/BreadcrumbList">
    <li itemprop="itemListElement" itemscope="" itemtype="http://schema.org/ListItem">
    <a class="bread-crumbs__item" href="/" itemprop="item">
    <span itemprop="name">
                    Home
                   </span>
    </a>
    <span class="hidden" itemprop="position">
                   1
                  </span>
    </li>
    <li itemprop="itemListElement" itemscope="" itemtype="http://schema.org/ListItem">
    <a class="bread-crumbs__item" href="/b/books/_/N-8q8" itemprop="item">
    <span itemprop="name">
                    Books
                   </span>
    </a>
    <span class="hidden" itemprop="position">
                   2
                  </span>
    </li>
    </ol>
    </nav>
    </div>
    <div class="pdp-base-container pt-0 book-item" id="productDetail">
    <div class="d-flex flex-wrap m-0" id="productDetail-container">
    <div class="pdp-section-spacing">
    </div>
    <div class="product-image-thumbnail product-detail-spacing p-0 m-0">
    <div class="d-sm-block d-lg-none" id="product-mobile-view-title">
    <header class="pdp-header bd-b-disabled-gray pb-s" id="prodSummary-header">
    <noscript>
    <img alt="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune" src="//prodimage.images-bn.com/pimages/9780593201893_p0_v3_s90x140.jpg"/>
    </noscript>
    <img alt="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune" class="Resolve lp-lazy" data-resolvechain="product=path[/pimages/9780593201893_p0_v3]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    <div class="header-content min-width-header-content" id="pdp-header-info">
    <h1 class="pdp-header-title text-lg-left text-sm-center mr-md-l ml-md-l mr-sm-l ml-sm-l" itemprop="name">
                      Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune
                     </h1>
    <input id="productName" type="hidden" value="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune"/>
    <div class="sticky-author" id="pdp-header-sticky-author">
    <div class="lists authors lists--unstyled text-lg-left text-sm-center" id="pdp-header-authors">
    <span class="contributors pdp-book-author" id="key-contributors">
                        by
                        <a href="/b/contributor/frank-herbert/_/N-2k97;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04">
                         Frank Herbert
                        </a>
    <input id="author" type="hidden" value="Frank Herbert"/>
    <input id="authorURL" type="hidden" value="/b/contributor/frank-herbert/_/N-2k97"/>
    <span href="/author/jd_salinger.html" itemprop="author" style="display:none">
                         Frank Herbert
                        </span>
    </span>
    </div>
    <div class="d-block">
    <div class="view-more text-sm-center text-lg-left">
    <a aria-expanded="false" class="down-arrowhead d-none" href="#">
                         View More
                        </a>
    </div>
    </div>
    </div>
    <div class="header-gigiya-wrapper mt-xs d-flex flex-lg-row flex-md-row flex-sm-column mt-lg-ss mt-sm-2 justify-content-lg-start justify-content-md-center" id="pdp-header-gigiya-wrapper">
    <div class="header-gigiya-inner star-rating d-flex justify-content-lg-start justify-content-sm-center" id="pdp-header-gigiya-inner">
    <div class="hidden-in-sticky">
    <div class="pdp-header-rating-gigiya" id="ratingsSocial">
    <span data-bv-product-id="9780593201893" data-bv-show="rating_summary" id="ratingsDisplay">
    </span>
    </div>
    <div class="editorial-review-header hidden">
    <span class="pipe">
                          |
                         </span>
    <a class="editorial-reviews-link" href="#EditorialReviews">
                          Editorial Reviews
                         </a>
    </div>
    </div>
    </div>
    </div>
    </div>
    </header>
    </div>
    <div class="row m-0">
    <input id="productSkuIdPdp" type="hidden" value="9780593201893"/>
    <div class="col-lg-12 product-image-img pl-xs pr-lg-xs pr-sm-0" id="prodImage">
    <div class="product-image-carousel pre-init" data-slick="{'accessibility':false}">
    <div class="product-image-slide" tabindex="-1">
    <div class="pdp-product-image-container" tabindex="-1">
    <div class="pdp-product-image pa-xs" tabindex="-1">
    <a data-liquiddomain="prodimage.images-bn.com" data-modal="%data-modal-url%" data-modal-class="BN.Modal.Browse.PDP.ImageViewer" data-modal-url="/modals/search/liquid-pixel-viewer.jsp?skuId=9780593201893" href="javascript:void(0);" tabindex="0" title="Click to Enlarge">
    <div class="bn-ProductBadge" id="bn-banner-container">
    <div class="bn-banner" style="background-color:#295A34">
                          BESTSELLER
                         </div>
    <div class="bn-triangle" style="border-top-color:#1D342A">
    </div>
    </div>
    <img alt="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune" class="Resolve full-shadow" data-bottom-align="" id="pdpMainImage" itemprop="image" src="//prodimage.images-bn.com/pimages/9780593201893_p0_v3_s600x595.jpg" tabindex="-1"/>
    </a>
    </div>
    </div>
    </div>
    </div>
    <div class="slick-image-dots d-flex justify-content-center">
    </div>
    <!-- Audiobook Sample Progress Bar -->
    <!-- Audiobook Sample Progress Bar -->
    <div class="mt-ss pdp-wishlist">
    <a aria-labelledby="add-wishlist" class="pdpAddToWishlistLink wish-list-item" data-url="/modals/account/add-to-wishlist-ra.jsp?skuId=9780593201893&amp;productId=prd9780593201893" href="#" rel="nofollow">
    <span class="icon icon-collection-default">
    </span>
    <span class="anchor-text" id="add-wishlist">
                      Add to Wishlist
                     </span>
    </a>
    </div>
    <section class="deal-badges d-lg-block d-md-none d-sm-none mt-s justify-content-center product-detail-spacing">
    <div class="productSeparator productSeparator-top-badge">
    </div>
    <!-- ATG-23625 Starts For Check Mark -->
    <div class="mb-xxs d-flex deal-badge-coupon">
    <div class="gc-coupon-icon">
    <span class="icon-check">
    </span>
    </div>
    <p class="ml-xxs promo-content mt-0 mb-0">
    <a class="one-column promo-link" href="https://www.barnesandnoble.com/b/dune-books/_/N-2vnl" onclick="set_cookie('pdpicon_Dune Books_na_text');" title="Dune Books &amp; More">
                       Dune Books &amp; More
                      </a>
    </p>
    </div>
    </section>
    </div>
    <script>
                   if(typeof performance.mark !== 'undefined' && typeof performance.measure !== 'undefined')
    {
    performance.mark('Cover_Image/Video_loading_ends');
    performance.measure(
    "coverImageVideoDur",
    "Cover_Image/Video_loading_starts",
    "Cover_Image/Video_loading_ends"
    );
    }
                  </script>
    </div>
    </div>
    <script>
                 if(typeof performance.mark !== 'undefined')
    {
    performance.mark('PDP_Commerce_Zone_loading_starts');
    }
                </script>
    <div class="commerce-zone-section sticky-cont header-section product-detail-spacing pl-s pr-lg-0" id="commerce-zone">
    <div class="sticky-left d-sm-none d-lg-block">
    <header class="pdp-header bd-b-disabled-gray pb-s" id="prodSummary-header">
    <noscript>
    <img alt="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune" src="//prodimage.images-bn.com/pimages/9780593201893_p0_v3_s90x140.jpg"/>
    </noscript>
    <img alt="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune" class="Resolve lp-lazy" data-resolvechain="product=path[/pimages/9780593201893_p0_v3]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    <div class="header-content min-width-header-content" id="pdp-header-info">
    <h1 class="pdp-header-title text-lg-left text-sm-center mr-md-l ml-md-l mr-sm-l ml-sm-l" itemprop="name">
                     Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune
                    </h1>
    <input id="productName" type="hidden" value="Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune"/>
    <div class="sticky-author" id="pdp-header-sticky-author">
    <div class="lists authors lists--unstyled text-lg-left text-sm-center" id="pdp-header-authors">
    <span class="contributors pdp-book-author" id="key-contributors">
                        by
                        <a href="/b/contributor/frank-herbert/_/N-2k97;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04">
                         Frank Herbert
                        </a>
    <input id="author" type="hidden" value="Frank Herbert">
    <input id="authorURL" type="hidden" value="/b/contributor/frank-herbert/_/N-2k97"/>
    <span href="/author/jd_salinger.html" itemprop="author" style="display:none">
                         Frank Herbert
                        </span>
    </input></span>
    </div>
    <div class="d-block">
    <div class="view-more text-sm-center text-lg-left">
    <a aria-expanded="false" class="down-arrowhead d-none" href="#">
                         View More
                        </a>
    </div>
    </div>
    </div>
    <div class="header-gigiya-wrapper mt-xs d-flex flex-lg-row flex-md-row flex-sm-column mt-lg-ss mt-sm-2 justify-content-lg-start justify-content-md-center" id="pdp-header-gigiya-wrapper">
    <div class="header-gigiya-inner star-rating d-flex justify-content-lg-start justify-content-sm-center" id="pdp-header-gigiya-inner">
    <div class="hidden-in-sticky">
    <div class="pdp-header-rating-gigiya" id="ratingsSocial">
    <span data-bv-product-id="9780593201893" data-bv-show="rating_summary" id="ratingsDisplay">
    </span>
    </div>
    <div class="editorial-review-header hidden">
    <span class="pipe">
                          |
                         </span>
    <a class="editorial-reviews-link" href="#EditorialReviews">
                          Editorial Reviews
                         </a>
    </div>
    </div>
    </div>
    </div>
    
    </div>
    </header>
    </div>
    <div class="commerce-zone sticky-right pdp-commerce-zone margin-left-for-sticky spinner-container">
    <div class="header-zone" id="prodPromo">
    <header class="d-sm-none d-lg-block">
    <h2 class="h2-as-h6 commerce-zone-format" href="http://schema.org/Paperback" id="pdp-info-format" itemprop="bookFormat">
                     Paperback
                    </h2>
    </header>
    <div class="d-sm-none d-lg-block">
    <div class="price-current-old-details">
    <span class="price current-price ml-0" id="pdp-cur-price">
                      $25.99
                     </span>
    <s class="old-price">
                      $30.97
                     </s>
    <span class="saved-percent discount-amount">
                      Save 16%
                     </span>
    <span class="sr-only" id="adaLabel">
                      Current price is $25.99, Original price is $30.97. You Save 16%.
                     </span>
    </div>
    </div>
    <div class="d-sm-block text-center d-lg-none">
    </div>
    <div class="d-lg-none d-sm-block">
    <ul class="pdp-refresh--buyoptns lists lists--unstyled purchase-options">
    <li class="purchase-options-item">
    <div class="radio-button-container" role="radiogroup">
    <div class="radio-wrapper">
    <label class="radio focus-state-label">
    <input checked="" id="shipping-purchase-optn" name="radio--puchase-optn" type="radio" value=""/>
    <span class="radio__circle radio__circle-format">
    </span>
    <div class="radio__text-container">
    <span class="radio__text tooltip-parent" data-trigger="">
    <header class="mt-sm-s mt-md-s">
    <h2 class="h2-as-h6 commerce-zone-format" href="http://schema.orgPaperback" id="pdp-info-format" itemprop="bookFormat">
                             Paperback
                            </h2>
    </header>
    </span>
    </div>
    </label>
    </div>
    </div>
    </li>
    <li class="purchase-options-item">
    <div class="radio-button-container" role="radiogroup">
    <div class="radio-wrapper">
    <label class="radio focus-state-label">
    <input checked="" id="shipping-purchase-optn" name="radio--puchase-optn" type="radio" value=""/>
    <span class="radio__circle radio__circle-format">
    </span>
    <div class="radio__text-container">
    <span class="radio__text tooltip-parent" data-trigger="">
    <div class="price-current-old-details">
    <span class="price current-price ml-0" id="pdp-cur-price">
                             $25.99
                            </span>
    <s class="old-price">
                             $30.97
                            </s>
    <span class="saved-percent discount-amount">
                             Save 16%
                            </span>
    <span class="sr-only" id="adaLabel">
                             Current price is $25.99, Original price is $30.97. You Save 16%.
                            </span>
    </div>
    </span>
    </div>
    </label>
    </div>
    </div>
    </li>
    </ul>
    </div>
    <div class="d-sm-none d-lg-block">
    </div>
    </div>
    <div class="d-block pick-up-cart mb-s">
    <div class="member-premium pt-4 text--center d-flex text-lg-left hidden-in-sticky d-none">
    <span class="icon-member-card pr-2">
    </span>
    <div class="float-left">
    <span class="premium-member-eligibility-msg">
    </span>
    <a class="line-height-link" href="/membership">
                      Learn more
                     </a>
    </div>
    </div>
    <ul class="pdp-refresh--buyoptns lists lists--unstyled purchase-options mt-m mt-md-xs mt-sm-xs">
    <li class="purchase-options-item purchase-add-to-cart">
    <div class="d-block pl-0 pr-0 shipping-msgs hidden-in-sticky">
    <div class="ship-this-item-txt bold-text">
                       SHIP THIS ITEM
                      </div>
    <div class="ship-this-item-qualify">
    <span>
                        Qualifies for Free Shipping
                       </span>
    <a aria-label="Free Shipping Tooltip" class="shipping-tooltip-icon tooltip-icon-info" data-classes="tooltip" data-modal-class="BN.Modal.Account.FreeShippingDetails" tabindex="0">
    </a>
    </div>
    <div class="shipping-message info-section">
    <div class="flex">
    <span class="icon-ship-truck mr-xs pt-xxxs">
    </span>
    <span class="shipping-message-text mt-0 mb-0">
                         Choose Expedited Shipping at checkout for delivery by
                         <span class="bold-text">
                          Thursday, April 4
                         </span>
    </span>
    </div>
    </div>
    </div>
    <div class="common-purchase-btn--container pr-0" id="addToCart">
    <div class="purchase-button-container d-md-flex d-lg-flex flex-sm-column" id="skuSelection">
    <div class="shipping-purchase-optn--formcont pdp-book-add-to-cart mr-md-4 mr-lg-0">
    <form action="/xhr/handler.jsp;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04?_DARGS=/cartridges/ProductDetailContent/ProductDetailTypes/includes/pdp-purchase-optns-new.jsp.frmbook_current" class="pdp-form shipping-purchase-optn--form" data-messaging="#pdpErrors" method="post">
    <input name="_dyncharset" type="hidden" value="UTF-8"/>
    <input name="_dynSessConf" type="hidden" value="-2943733321097363530"/>
    <input id="addItmPdp-sku" name="/atg/commerce/order/purchase/CartModifierFormHandler.catalogRefIds" type="hidden" value="9780593201893"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.catalogRefIds" type="hidden" value=" "/>
    <input class="add-to-cart-button btn-addtocart btn-pdp-addtocart btn btn--commerce btn--commerce-non-digital" type="submit" value="ADD TO CART"/>
    <input id="pEAN" type="hidden" value="9780593201893"/>
    <input id="parentSku" type="hidden" value="1136810577">
    <input id="skuType" type="hidden" value="book">
    <input id="availability" type="hidden" value="1000"/>
    <input id="isEligibleForFreeShipping" type="hidden" value="true"/>
    <input id="isAudiobookProduct" type="hidden" value="false"/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.quantity" type="hidden" value="1"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.quantity" type="hidden" value=" "/>
    <input id="addItmPdp-prodid" name="/atg/commerce/order/purchase/CartModifierFormHandler.productId" type="hidden" value="prd9780593201893"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.productId" type="hidden" value=" "/>
    <input name="amplifiHandler" type="hidden" value="/atg/commerce/order/purchase/CartModifierFormHandler.addItemToOrder"/>
    <input name="_DARGS" type="hidden" value="/cartridges/ProductDetailContent/ProductDetailTypes/includes/pdp-purchase-optns-new.jsp.frmbook_current">
    </input>
    </input>
    </input>
    </form>
    <div class="ip--formcont ip-purchase-optn--formcont hidden-in-sticky mt-sm-xs">
    <form action="/xhr/handler.jsp;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04?_DARGS=/cartridges/ProductDetailContent/ProductDetailTypes/includes/pdp-purchase-optns-new.jsp.frmbook_current_instant" class="ip-form" method="post">
    <input name="_dyncharset" type="hidden" value="UTF-8"/>
    <input name="_dynSessConf" type="hidden" value="-2943733321097363530"/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.quantity" type="hidden" value="1"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.quantity" type="hidden" value=" "/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.catalogRefIds" type="hidden" value="9780593201893"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.catalogRefIds" type="hidden" value=" "/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.productId" type="hidden" value="prd9780593201893"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.productId" type="hidden" value=" "/>
    <div class="WPCommonHiddenFields">
    </div>
    <input class="checkoutId" id="response$checkoutId" name="/atg/commerce/order/purchase/CartModifierFormHandler.cvv" type="hidden" value=""/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.cvv" type="hidden" value=" "/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchaseCartURL" type="hidden" value="/checkout/"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchaseCartURL" type="hidden" value=" "/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchaseShippingURL" type="hidden" value="/checkout/shipping.jsp"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchaseShippingURL" type="hidden" value=" "/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchasePaymentURL" type="hidden" value="/checkout/payment.jsp"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchasePaymentURL" type="hidden" value=" "/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchaseReviewURL" type="hidden" value="/checkout/review.jsp"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchaseReviewURL" type="hidden" value=" "/>
    <input name="/atg/commerce/order/purchase/CartModifierFormHandler.fromAudioBook" type="hidden" value="false"/>
    <input name="_D:/atg/commerce/order/purchase/CartModifierFormHandler.fromAudioBook" type="hidden" value=" "/>
    <input name="xhrRedirect" type="hidden" value="/checkout/thank-you.jsp"/>
    <input class="btn-instant-purchase btn btn--commerce-secondary strict-hidden disabled" disabled="" type="submit" value="Instant Purchase"/>
    <input name="amplifiHandler" type="hidden" value="/atg/commerce/order/purchase/CartModifierFormHandler.instantPurchase"/>
    <input name="isInstantPurchase" type="hidden" value="true"/>
    <input name="skuId" type="hidden" value="9780593201893"/>
    <button class="sign-in-instant-purchase btn btn--commerce-secondary pl-5 pr-5 disabled" disabled="">
                                Instant Purchase
                               </button>
    <input class="formCVVCode" data-skuid="9780593201893" minlength="" type="hidden">
    <input name="_DARGS" type="hidden" value="/cartridges/ProductDetailContent/ProductDetailTypes/includes/pdp-purchase-optns-new.jsp.frmbook_current_instant">
    </input>
    </input>
    </form>
    </div>
    </div>
    </div>
    </div>
    </li>
    <li class="purchase-options-item">
    <div class="shipping-msgs hidden-in-sticky d-block pl-0">
    <script>
                       if(typeof performance.mark !== 'undefined')
    performance.mark("PDP_bopis_functionality_loading_starts");
                      </script>
    <div class="pick-up-msg" data-trigger="">
                       PICK UP IN STORE
                      </div>
    <span class="radio--link">
    <a class="open-ss-modal mg-store" data-skuid="9780593201893" href="javascript:void(0);" tabindex="0">
                        Check Availability at Nearby Stores
                       </a>
    </span>
    </div>
    <div class="common-purchase-btn--container pickup pr-0 d-block" id="ropisReserveLink">
    <input id="changeStoreBtnPosition" type="hidden" value="page"/>
    <input id="isRopisEnabled" type="hidden" value="true"/>
    <input id="currStoreName" type="hidden" value=""/>
    <input id="currStoreID" type="hidden" value=""/>
    <input id="eligibleMessageUpdated" type="hidden" value="storeNotAvailable"/>
    <input id="storeName" type="hidden" value=""/>
    <input id="storeID" type="hidden" value=""/>
    <input id="isBopisOptnRadio" type="hidden" value="true"/>
    <input id="addToCartSuccessModalOpenFrom" type="hidden" value="pdp"/>
    <input class="add-to-cart-button btn-addtocart btn-pdp-addtocart btn btn--commerce btn-pick-up no-click" id="openReserveModal" type="submit" value="Unavailable for Pickup">
    <p class="mb-0 mt-xs text-center availability-time hidden-in-sticky d-none">
                                Available within 2 business hours
                               </p>
    </input>
    </div>
    </li>
    </ul>
    <ul class="wish-list d-sm-none d-lg-none" role="presentation">
    <li>
    <a aria-labelledby="store-availability" class="wish-list-item" data-modal-class="BN.Modal.Browse.PDP.ReserveTT" href="#">
    <span class="icon icon-location-circle">
    </span>
    <span class="anchor-text in-store" id="store-availability">
                       Want it Today?
                       <br/>
    <span class="in-store-available">
                        Check Store Availability
                       </span>
    </span>
    </a>
    </li>
    </ul>
    </div>
    <section class="deal-badges d-lg-none d-md-block d-sm-block mb-s" id="pdp-tabs">
    <h2 class="d-sm-block pb-s d-md-block d-lg-none">
                    Related collections and offers
                   </h2>
    <div class="productSeparator productSeparator-top-badge">
    </div>
    <!-- ATG-23625 Starts For Check Mark -->
    <div class="mb-xxs d-flex deal-badge-coupon">
    <div class="gc-coupon-icon">
    <span class="icon-check">
    </span>
    </div>
    <p class="ml-xxs promo-content mt-0 mb-0">
    <a class="one-column promo-link" href="https://www.barnesandnoble.com/b/dune-books/_/N-2vnl" onclick="set_cookie('pdpicon_Dune Books_na_text');" title="Dune Books &amp; More">
                      Dune Books &amp; More
                     </a>
    </p>
    </div>
    </section>
    <div class="d-none hidden-in-sticky stamp-msg-rewards">
    <span class="icon-member-stamp mr-xs">
    </span>
    <div class="member-stamp-shipping-message-text">
    </div>
    </div>
    <ul class="wish-list d-sm-none d-lg-none" role="presentation">
    <li>
    <a aria-labelledby="store-availability" class="wish-list-item" data-modal-class="BN.Modal.Browse.PDP.ReserveTT" href="#">
    <span class="icon icon-location-circle">
    </span>
    <span class="anchor-text in-store" id="store-availability">
                      Want it Today?
                      <br/>
    <span class="in-store-available">
                        Check Store Availability
                       </span>
    </span>
    </a>
    </li>
    </ul>
    <div class="wishlist-on-sticky">
    <a aria-label="Add to Wishlist" class="pdpAddToWishlistLink wish-list-item" data-url="/modals/account/add-to-wishlist-ra.jsp?skuId=9780593201893&amp;productId=prd9780593201893" href="#" rel="nofollow">
    <span class="icon icon-collection-default">
    </span>
    </a>
    </div>
    </div>
    </div>
    <div class="sticky-commerce-mobile pdp-commerce-zone d-none d-lg-none">
    <div class="d-flex">
    <div class="add-to-cart-btn-container sticky-mobile-cart mb-xs">
    </div>
    <div class="pickup-btn-container">
    </div>
    </div>
    <div class="out-of-stock-msg">
    </div>
    <div class="pricing-section">
    </div>
    </div>
    <script>
                 if(typeof performance.mark !== 'undefined' && typeof performance.measure !== 'undefined')
    {
    performance.mark('PDP_Commerce_Zone_loading_ends');
    performance.measure(
    "pdpCommerceDur",
    "PDP_Commerce_Zone_loading_starts",
    "PDP_Commerce_Zone_loading_ends"
    );
    }
                </script>
    </div>
    </div>
    </section>
    <meta content="2020-08-25" itemprop="datePublished"/>
    <span class="hidden" itemprop="inLanguage">
               English
              </span>
    <span class="hidden" itemprop="isbn">
               0593201892
              </span>
    <div class="hidden" itemprop="offers" itemscope="" itemtype="http://schema.org/Offer">
    <meta content="USD" itemprop="priceCurrency">
    <link href="/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893" itemprop="url">
    <span itemprop="price">
                25.99
               </span>
    <link href="http://schema.org/InStock" itemprop="availability">
               In Stock
              </link></link></meta></div>
    
    </div>
    <!-- ticket number ATG-18566:Product Bundle start -->
    <!-- ticket number ATG-18566:Product Bundle end -->
    <input id="primayCategoryId" type="hidden" value="p4667"/>
    <input id="subCategoryIds" type="hidden" value="[p8998, 2798851, 2796683, 3335442, p431, 3652453, p7777, 2916841, p9409, p145]"/>
    <script>
               if(typeof performance.mark !== 'undefined' && typeof performance.measure !== 'undefined')
    {
    performance.mark("Above_the_fold_loading_ends");
    performance.measure(
    "ATFDur",
    "Above_the_fold_loading_starts",
    "Above_the_fold_loading_ends"
    );
    }
              </script>
    <hr class="overview-divider-width pdp-ov-section-divider-line mt-ss mb-0 d-sm-block d-lg-none"/>
    <div class="pt-m mb-l bs-ov-section" id="overviewSection">
    <div class="bs-ov-cont">
    <div class="content overview-expandable-section">
    <h2 class="bs-ov-header p-0">
                  Overview
                 </h2>
    <div class="text--medium overview-content p-lg-4 p-sm-0 bookseller-cont">
    <div class="bs-content">
    <div class="overview-cntnt" itemprop="description">
    <b>
                     Perfect for longtime fans and new readers alike—a beautiful premium mass market boxed set of the first three novels in Frank Herbert's Dune Saga.
                     <br/>
    </b>
    <br/>
                    In the far future, on a remote planet, an epic adventure awaits. Here are the first three novels of Frank Herbert’s magnificent Dune saga—a triumph of the imagination and one of the bestselling science fiction series of all time.
                    <br/>
    <br/>
    <b>
                     Includes Books 1 - 3: DUNE • DUNE MESSIAH • CHILDREN OF DUNE
                     <br/>
    <br/>
    </b>
                    • DUNE: PART TWO • THE MAJOR MOTION PICTURE NOW IN THEATERS
                    <br/>
                    Directed by Denis Villeneuve, screenplay by Denis Villeneuve and Jon Spaihts, based on the novel
                    <i>
                     Dune
                    </i>
                    by Frank Herbert • Starring Timothée Chalamet, Zendaya, Rebecca Ferguson, Josh Brolin, Austin Butler, Florence Pugh, Dave Bautista, Christopher Walken, Léa Seydoux, with Stellan Skarsgård, with Charlotte Rampling, and Javier Bardem
                   </div>
    </div>
    </div>
    <hr class="pdp-ov-section-divider-line mt-ss mb-0 d-sm-block d-lg-none"/>
    </div>
    </div>
    </div>
    <input id="seriesCount" type="hidden" value="5253904"/>
    <section class="pb-0 text--center" data-cache="" data-languagelink="/b/_/N-1z141wb" data-serieslink="/b/series/dune-chronicles-series/_/N-2kpe" data-seriesnumber="" data-skuid="9780593201893" data-skutype="book" data-title="More in This Series" data-workid="1136810577" id="moreInThisSeriesSection">
    <div class="spinner spinner__medium">
    <img aria-label="Loading ..." aria-live="polite" role="presentation" src="//img.images-bn.com/static/redesign/srcs/images/spinner.svg" tabindex="0"/>
    </div>
    </section>
    <section class="pb-0 text--center" data-cache="true" data-fromwl="" data-skuid="9780593201893" data-skutype="book" data-title="You May Also Like" id="recommendations">
    <div class="spinner spinner__medium">
    <img aria-label="Loading ..." aria-live="polite" role="presentation" src="//img.images-bn.com/static/redesign/srcs/images/spinner.svg" tabindex="0"/>
    </div>
    </section>
    <script>
                if(typeof performance.mark !== 'undefined')
    performance.mark("Product_Tabs_loading_start");
               </script>
    <!-- Code Change For ATG-10237,Starts -->
    <!-- Code Change For ATG-10391,Starts-->
    <!-- Code Change For ATG-10391,Ends-->
    <!-- Code Change For ATG-10237,Ends-->
    <section class="mb-m mt-m" id="pdp-tabs">
    <div class="tab-container" data-tabs='{"autosize": true}' id="pdp-tab-container" tabindex="-1">
    <div class="tab-list-container text--center">
    <input id="pdpContentTabLimit" name="pdpContentTabLimit" type="hidden" value="4"/>
    <ul class="tab-list" id="productInfoTabs" role="tablist">
    <li class="prodtabs">
    <a aria-controls="ProductDetailsTab" aria-selected="true" class="tab" href="#ProductDetailsTab" role="tab">
                      Product Details
                     </a>
    </li>
    <!-- Code Change For ATG-10237,Starts -->
    <!-- Code Change For ATG-10237,Ends -->
    <li role="presentation">
    <a aria-controls="MeetTheAuthor" aria-selected="true" class="tab" href="#MeetTheAuthor" role="tab">
                      About the Author
                     </a>
    </li>
    </ul>
    <div class="tab-highlight d-none d-lg-block">
    </div>
    </div>
    <div class="tabpanels-container d-none d-lg-block">
    <div class="tabpanels">
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    <div class="tabpanel" id="ProductDetailsTab" role="tabpanel" tabindex="-1">
    <h2 class="text--center mb-s">
                      Product Details
                     </h2>
    <table class="plain centered">
    <tbody>
    <!-- changes start for ATG-9471 -->
    <tr>
    <th>
                         ISBN-13:
                        </th>
    <!-- changes End for ATG-9471 -->
    <td>
                         9780593201893
                        </td>
    </tr>
    <tr>
    <th>
                         Publisher:
                        </th>
    <td>
    <a href="/s/%22Penguin+Publishing+Group%22;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04?Ntk=Publisher&amp;Ns=P_Sales_Rank&amp;Ntx=mode+matchall">
    <span itemprop="publisher">
                           Penguin Publishing Group
                          </span>
    </a>
    </td>
    </tr>
    <tr>
    <th>
                         Publication date:
                        </th>
    <td>
                         08/25/2020
                        </td>
    </tr>
    <tr>
    <th>
                         Series:
                        </th>
    <td>
    <a href="/b/series/dune-chronicles-series/_/N-2kpe">
                          Dune Chronicles Series
                         </a>
    </td>
    </tr>
    <tr>
    <th>
                         Sales rank:
                        </th>
    <td>
                         99
                        </td>
    </tr>
    <tr>
    <th>
                         Product dimensions:
                        </th>
    <td>
                         4.40(w) x 7.70(h) x 4.20(d)
                        </td>
    </tr>
    <tbody>
    </tbody>
    </tbody>
    </table>
    </div>
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    <!-- Code Change For ATG-10237,Starts -->
    <!-- Code Change For ATG-10237,Ends -->
    <!-- Code Change For ATG-10237,Starts  -->
    <!--  Code Change For ATG-10237,Ends -->
    <div class="tabpanel" id="MeetTheAuthor" role="tabpanel" tabindex="-1">
    <h2 class="text--center mb-s">
                      About the Author
                     </h2>
    <div class="row">
    <!-- ATG-10370 : Adding header after empty check for image-->
    <div class="col-lg-4 pr-m">
    <noscript>
    <img alt="" class="block" src="https://prodimage.images-bn.com/cimages/0000000148160_p0_v4_s681x516.jpg"/>
    </noscript>
    <img alt="About The Author" class="Resolve lp-lazy block imag" data-resolvechain="product=path[/cimages/0000000148160_p0_v4]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </div>
    <!-- ATG-10370 : Adding header after empty check for content and image-->
    <div class="expandable-section col-lg-8">
    <div class="text--medium summarized">
    <b>
                         Frank Herbert
                        </b>
                        is the bestselling author of the Dune saga. He was born in Tacoma, Washington, and educated at the University of Washington, Seattle. He worked a wide variety of jobs—including TV cameraman, radio commentator, oyster diver, jungle survival instructor, lay analyst, creative writing teacher, reporter and editor of several West Coast newspapers—before becoming a full-time writer.
                        <br/>
    <br/>
                        In 1952, Herbert began publishing science fiction with “Looking for Something?” in
                        <i>
                         Startling Stories
                        </i>
                        . But his emergence as a writer of major stature did not occur until 1965, with the publication of
                        <i>
                         Dune
                        </i>
                        .
                        <i>
                         Dune Messiah
                        </i>
                        ,
                        <i>
                         Children of Dune
                        </i>
                        ,
                        <i>
                         God Emperor of Dune
                        </i>
                        ,
                        <i>
                         Heretics of Dune
                        </i>
                        , and
                        <i>
                         Chapterhouse: Dune
                        </i>
                        followed, completing the saga that the
                        <i>
                         Chicago Tribune
                        </i>
                        would call “one of the monuments of modern science fiction.” Herbert is also the author of some twenty other books, including
                        <i>
                         The White Plague
                        </i>
                        ,
                        <i>
                         The Dosadi Experiment
                        </i>
                        , and
                        <i>
                         Destination: Void
                        </i>
                        . He died in 1986.
                       </div>
    <!-- ATG-10370 : Adding header after empty check for image, content and authorbiocommentary -->
    </div>
    <div class="text--center w-100 mt-s">
    <a aria-expanded="false" class="read-more show-more-pdp" href="javascript:void(0);">
                        Show More
                       </a>
    </div>
    </div>
    </div>
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    <div class="tabpanel pb-0 pt-0" role="tabpanel">
    </div>
    </div>
    </div>
    </div>
    </section>
    <script>
                if(typeof performance.mark !== 'undefined' && typeof performance.measure !== 'undefined')
    {
    performance.mark("Product_Tabs_loading_end");
    performance.measure(
    "productTabsDur",
    "Product_Tabs_loading_start",
    "Product_Tabs_loading_end"
    );
    }
               </script>
    <div class="content-node sweepstakes">
    <section class="container container--no-padding-bottom sweep-stake-section pl-0 pr-0" id="pdp-sweepstakes" style="padding-top:0!important; padding-bottom:0!important;">
    <div class="sweep-stake-main-container custom-blog-container">
    </div>
    <div class="clear">
    </div>
    </section>
    <script type="text/javascript">
                 (function(){
    var isPreviewEnv = false;
    if (window.location.hostname === "prodny-endeca.bn-web.com" || window.location.hostname === "prodny-preview.bn-web.com" || window.location.hostname === "qa2-preview2.bn-web.com" || window.location.hostname === "localhost"){isPreviewEnv = true;}
    var BNgetQSParams = function (sParam) {
    var sPageURL = window.location.search.substring(1);
    var sURLVariables = sPageURL.split("&");
    for (var i = 0; i < sURLVariables.length; i++) {
    var sParameterName = sURLVariables[i].split("=");
    if (sParameterName[0] === sParam) {
    return sParameterName[1];
    }
    }
    };
    var todaysDate = new Date();
    var todayOrPreviewDate = todaysDate;
    var endecaParam = BNgetQSParams("Endeca_date");
    if(isPreviewEnv && endecaParam){
    endecaParam = endecaParam.substring(0, 10);
    endecaParam = endecaParam.replace(/\-/g, '/');
    var endecaDate = new Date(endecaParam);
    if(endecaDate > todaysDate){ todayOrPreviewDate = endecaDate;}
    }
    
    window.sweepsData = [
    
    
    
    {
    "count": "1",
    "workid": "1144121772",
    "headerMain": "Sweepstakes",
    "title": "&quot;A Novel Love Story&quot; by Ashley Poston Sweepstakes",
    "copy": "Pre-order <i>A Novel Love Story</i> to be automatically entered for a chance to win a candle, a reading shawl, a mug and tea, and a $150 Barnes & Noble gift card!",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/a-novel-love-story-sweepstakes-rules.use.html",
    "startDate": "01/16/2024",
    "endDate": "06/24/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "2",
    "workid": "1144107851",
    "headerMain": "Sweepstakes",
    "title": "&quot;All Fours&quot; by Miranda July Sweepstakes",
    "copy": "Pre-order <em>All Fours</em> for a chance to win a $150 Dusen & Dusen gift card, a RoomLift virtual design consultation on the room of your choice and more!",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/all-fours-by-miranda-july-sweepstakes-rules.use.html",
    "startDate": "01/17/2024",
    "endDate": "05/13/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/AllFoursSweepstakesImage.jpg',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/AllFoursSweepstakesImage.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "3",
    "workid": "1144510818",
    "headerMain": "Sweepstakes",
    "title": "&quot;Throne of Secrets&quot; by Kerri Maniscalco Sweepstakes",
    "copy": "Pre-order <em>Throne of Secrets</em> for a chance to win a custom Mage of Metals necklace, signed copies of <em>Throne of the Fallen</em> and <em>Throne of Secrets</em>, and a $100 B&N gift card!",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/throne-of-secrets-sweepstakes-rules.use.html",
    "startDate": "02/22/2024",
    "endDate": "09/23/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "4",
    "workid": "1144768860",
    "headerMain": "Sweepstakes ",
    "title": "&quot;Love, Mom&quot; by Nicole Saphier Sweepstakes",
    "copy": "Pre-order <em>Love, Mom</em> to be automatically entered for a chance to win a Thank You, Mom Homesick candle, a Brooklinen sleep mask, a $100 Barnes & Noble gift card and more. Runs 2/14/24 - 4/15/24. No purchase necessary. U.S. residents 18+ only.",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/love-mom-sweeps-rules.use.html",
    "startDate": "02/14/2024",
    "endDate": "04/15/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "5",
    "workid": "1144089485",
    "headerMain": "Sweepstakes",
    "title": "&quot;A Calamity of Souls&quot; by David Baldacci Sweepstakes",
    "copy": "Pre-order <em>A Calamity of Souls</em> for a chance to win a $100 Barnes & Noble gift card, a Virginia Homesick candle, a leather planner and a signed copy of the book!",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/a-calamity-of-souls-sweepstakes-rules.use.html",
    "startDate": "02/21/2024",
    "endDate": "04/15/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "6",
    "workid": "1144699761",
    "headerMain": "Sweepstakes",
    "title": "&quot;Husbands & Lovers&quot; by Beatriz Williams Sweepstakes",
    "copy": "Pre-order <em>Husbands & Lovers</em> to be automatically entered for a chance to win a gold cobra bracelet, a signed copy of the book, and a $100 Barnes & Noble gift card!",
    "detailsCta":"See details and official rules here. ",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/husbands-and-lovers-sweepstakes-rules.use.html",
    "startDate": "01/30/2024",
    "endDate": "06/24/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/02/Husbands_and_Lovers_Sweepstakes.jpg',
    "alt": "Associated products including B&N Gift Card, Gold Snake Bracelet, & Husbands & Lovers by Beatriz Williams. Available 6/25.",
    "defaultImagePath": "/content/dam/ccr/Sweepstakes/2024/02/Husbands_and_Lovers_Sweepstakes.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/02/Husbands_and_Lovers_Sweepstakes.jpg",
    "displayAlt": "Associated products including B&N Gift Card, Gold Snake Bracelet, & Husbands & Lovers by Beatriz Williams. Available 6/25."},
    
    
    
    {
    "count": "7",
    "workid": "1143813811",
    "headerMain": "Sweepstakes",
    "title": "&quot;Home Is Where The Bodies Are&quot; by Jeneva Rose Sweepstakes",
    "copy": "Pre-order <em>Home is Where the Bodies Are</em> for a chance to win a bluetooth projector, a Harry & David movie night gift basket, and a $250 Vudu gift card!",
    "detailsCta":"See details and official rules here. ",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2023/12/home-is-where-the-bodies-are-sweeps-rules.use.html",
    "startDate": "12/26/2023",
    "endDate": "04/29/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "8",
    "workid": "1143886130",
    "headerMain": "Sweepstakes",
    "title": "&quot;Just for the Summer&quot; by Abby Jimenez Sweepstakes",
    "copy": "Pre-order <em>Just for the Summer</em> for a chance to win a dozen cupcakes from Nadia Cakes, a $100 Barnes & Noble gift card, a glitter unicorn floatie and more!",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/just-for-the-summer-sweepstakes-rules.use.html",
    "startDate": "02/21/2024",
    "endDate": "04/01/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "9",
    "workid": "1144178271",
    "headerMain": "Sweepstakes",
    "title": "The &quot;Discovering Daniel&quot; Sweepstakes",
    "copy": "Pre-order <em>Discovering Daniel</em> to be automatically entered for a chance to win a signed copy of <em>Discovering Daniel</em>, a 10th generation iPad, and a $125 Barnes & Noble gift card.",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/discovering-daniel-sweeps-rules.use.html",
    "startDate": "03/26/2024",
    "endDate": "05/06/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "10",
    "workid": "1137164322",
    "headerMain": "Sweepstakes",
    "title": "&quot;If We Ever Meet Again&quot; by Ana Huang Sweepstakes",
    "copy": "Pre-order <i>If We Ever Meet Again</i> for a chance to win a Beis Atlas Pink carry on roller bag and mini weekender bag!",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/if-we-ever-meet-again-sweepstakes-rules.use.html",
    "startDate": "01/23/2024",
    "endDate": "06/24/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "11",
    "workid": "1144709315",
    "headerMain": "Sweepstakes",
    "title": "&quot;Trick or Treat on Scary Street&quot; by Lance Bass Sweepstakes",
    "copy": "Pre-order <i>Trick or Treat on Scary Street</i> to be automatically entered for a chance to win vinyl records of *NSYNC, Home for Christmas and No Strings Attached signed by Lance Bass, a $100 Barnes & Noble gift card, and a signed copy of <i>Trick or Treat on Scary Street</i>! ",
    "detailsCta":"See details and official rules here. ",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/trick-or-treat-on-scary-street-sweeps-rules.use.html",
    "startDate": "01/24/2024",
    "endDate": "07/22/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "12",
    "workid": "1143849280",
    "headerMain": "Sweepstakes",
    "title": "&quot;The Paris Novel&quot; by Ruth Reichl Sweepstakes",
    "copy": "Pre-order <i>The Paris Novel</i> to be automatically entered for a chance to win an online French cooking class, a tote bag, signed Ruth Reichl books, and a $200 Le Creuset gift card!",
    "detailsCta":"See details and official rules here. ",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/the-paris-novel-by-ruth-reichl-sweeps-rules.use.html",
    "startDate": "01/25/2024",
    "endDate": "04/22/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "13",
    "workid": "1144040367",
    "headerMain": "Sweepstakes",
    "title": "&quot;Blood at the Root&quot; by LaDarrion Williams Sweepstakes",
    "copy": "<p>Pre-order <em>Blood at the Root</em> to be automatically entered for a chance to win a Caiman University pennant and hoodie, a Fossil leather backpack, a 2024 Task calendar and a Stanley tumbler!",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/blood-at-the-root-sweepstakes.use.html",
    "startDate": "01/26/2024",
    "endDate": "05/06/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/BloodRoot_BN_Sweeps_Products_V3.jpg',
    "alt": "Bloodroot Sweepstakes with Caiman University Banner, leather book bag, branded sweater and water bottle.",
    "defaultImagePath": "/content/dam/ccr/Sweepstakes/2024/03/BloodRoot_BN_Sweeps_Products_V3.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/BloodRoot_BN_Sweeps_Products_V3.jpg",
    "displayAlt": "Bloodroot Sweepstakes with Caiman University Banner, leather book bag, branded sweater and water bottle."},
    
    
    
    {
    "count": "14",
    "workid": "1144604231",
    "headerMain": "Sweepstakes",
    "title": "&quotThe Thirteenth Child&quot by Erin A. Craig Sweepstake",
    "copy": "Pre-order <em>The Thirteenth Child</em> to be automatically entered for a chance to win a Grimm’s Complete Fairy Tales book, a candle, a leather book necklace, and a $150 Barnes & Noble gift card!",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/the-thirteenth-child-sweepstakes.use.html",
    "startDate": "01/26/2024",
    "endDate": "09/23/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/ThirteenthChild_BN_Sweeps_Products_LR.jpg',
    "alt": "Grimm's Complete Fairy Tales, B&N Gift Card and Candle Smells like she's reading Erin A. Craig Again.",
    "defaultImagePath": "https://dispatch.barnesandnoble.com/content/dam/ccr/Sweepstakes/2024/03/ThirteenthChild_BN_Sweeps_Products_LR.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/ThirteenthChild_BN_Sweeps_Products_LR.jpg",
    "displayAlt": "Grimm's Complete Fairy Tales, B&N Gift Card and Candle Smells like she's reading Erin A. Craig Again."},
    
    
    
    {
    "count": "15",
    "workid": "1143636259",
    "headerMain": "Sweepstakes",
    "title": "&quotA Whisper in the Walls&quot Sweepstakes",
    "copy": "Pre-order <em>A Whisper in the Walls</em> for a chance to win signed hardcover copies of <em>A Door in the Dark</em> and <em>A Whisper in the Walls</em>, a leather-bound journal with journaling pens, a hawk ring, and more!",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/1/a-whisper-in-the-walls-sweepstakes.use.html",
    "startDate": "01/26/2024",
    "endDate": "04/22/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "16",
    "workid": "1144086478",
    "headerMain": "Sweepstakes",
    "title": "&quotPlantYou: Scrappy Cooking&quot by Carleigh Bodrug Sweepstakes",
    "copy": "Pre-order <em>PlantYou: Scrappy Cooking</em> for a chance to win a $100 Barnes & Noble gift card, a signed copy of the book, and a Vitamix! ",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/plantyou-scrappy-cooking-sweeps-rules.use.html",
    "startDate": "03/08/2024",
    "endDate": "04/01/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/PlantYou_Scrappy_Cooking_sweeps.jpg',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/Sweepstakes/2024/03/PlantYou_Scrappy_Cooking_sweeps.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/PlantYou_Scrappy_Cooking_sweeps.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "17",
    "workid": "1144227069",
    "headerMain": "Sweepstakes",
    "title": "&quot;Reckless&quot; by Lauren Roberts Sweepstakes",
    "copy": "Pre-order <em>Reckless</em> for a chance to win signed Exclusive Editions of <em>Reckless</em>, <em>Powerless</em>, and <em>Powerful</em>, and a &quot;start your own writing journey&quot; essential kit including an iPad with keyboard, a Bluetooth mouse and more!",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/reckless-sweepstakes.use.html",
    "startDate": "02/21/2024",
    "endDate": "07/01/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "18",
    "workid": "1143595985",
    "headerMain": "Sweepstakes",
    "title": "&quotSong of the Six Realms&quot by Judy I.Lin Sweepstakes",
    "copy": "Pre-order <em>Song of the Six Realms</em> to be automatically entered for a chance to win signed copies of <em>Song of the Six Realms</em>, <em>A Magic Steeped in Poison</em>, and <em>A Venom Dark and Sweet</em>, a musical jewelry box, incense and more!",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/song-of-six-realms-sweepstakes.use.html",
    "startDate": "02/14/2024",
    "endDate": "04/22/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "19",
    "workid": "1144612817",
    "headerMain": "Sweepstakes",
    "title": "&quot;What to Cook When You Don't Feel Like Cooking&quot; by Caroline Chambers",
    "copy": "Pre-order <em>What to Cook When You Don't Feel Like Cooking</em> to be automatically entered for a chance to win a Vitamix 64-oz blender, a one-year subscriptions to Caroline Chambers's Substack, and a signed copy of the book!",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/what-to-cook-sweeps-rules.use.html",
    "startDate": "02/27/2024",
    "endDate": "08/12/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "20",
    "workid": "1144200779",
    "headerMain": "Sweepstakes",
    "title": "&quot;By Any Other Name&quot; by Jodi Picoult",
    "copy": "Pre-order <em>By Any Other Name</em>to be automatically entered for a chance to win flowers, a Calligraphy class, a candle, and an online subscription to Shakespeare’s Globe Theatre. The sweepstakes ends August 19th, 2024.",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/by-any-other-name-sweepstakes-rules.use.html",
    "startDate": "02/29/2024",
    "endDate": "08/19/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/ByAnyOtherName_Sweeps_Image.jpg',
    "alt": "flowers, an online Calligraphy class, a candle, and an online subscription to Shakespeare’s Globe Theatre",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/ByAnyOtherName_Sweeps_Image.jpg",
    "displayAlt": "flowers, an online Calligraphy class, a candle, and an online subscription to Shakespeare’s Globe Theatre"},
    
    
    
    {
    "count": "21",
    "workid": "1143889870",
    "headerMain": "Sweepstakes",
    "title": "&quot;The Summer Pact&quot; by Emily Giffin Sweepstakes",
    "copy": "Pre-order <em>The Summer Pact</em> to be automatically entered for a chance to win a Stamos Bien tote bag, BFF candle, a $150 AirBnB gift card, a signed copy of the book, and more! The sweepstakes ends July 8, 2024.",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/2/the-summer-pact-sweepstakes-rules.use.html",
    "startDate": "02/29/2024",
    "endDate": "07/08/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/02/The_Summer_Pact_Sweeps_Image.jpg',
    "alt": "Signed Copy of The Summer Pact by Emily Griffen, Sunflowers, tote bag and assorted confections",
    "defaultImagePath": "/content/dam/ccr/Sweepstakes/2024/02/The_Summer_Pact_Sweeps_Image.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/02/The_Summer_Pact_Sweeps_Image.jpg",
    "displayAlt": "Signed Copy of The Summer Pact by Emily Griffen, Sunflowers, tote bag and assorted confections"},
    
    
    
    {
    "count": "22",
    "workid": "1144797874",
    "headerMain": "Sweepstakes",
    "title": "&quot;The Glass Girl&quot; by Kathleen Glasgow Sweepstakes",
    "copy": "Pre-order <em>The Glass Girl</em> to be automatically entered for a chance to win a weighted blanket, a journal and a Hatch sleep machine! ",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/the-glass-girl-sweepstakes.use.html",
    "startDate": "03/05/2024",
    "endDate": "11/11/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/GlassGirl_BN_Sweeps_Products.jpg',
    "alt": "The Glass Girl book, diffuser, and gray throw.",
    "defaultImagePath": "/content/dam/ccr/Sweepstakes/2024/03/GlassGirl_BN_Sweeps_Products.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/GlassGirl_BN_Sweeps_Products.jpg",
    "displayAlt": "The Glass Girl book, diffuser, and gray throw."},
    
    
    
    {
    "count": "23",
    "workid": "1144329347",
    "headerMain": "Sweepstakes",
    "title": "&quot;Little People, Big Dreams: Taylor Swift&quot; by Maria Isabel Sanchez Vegara Sweepstakes",
    "copy": "Pre-order <em>Little, People, Big Dreams: Taylor Swift</em> to be automatically entered for a chance to win a Little People, Big Dreams library and a Taylor Swift-branded acoustic guitar!",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/taylor-swift-little-people-big-dreams-sweepstakes.use.html",
    "startDate": "03/08/2024",
    "endDate": "06/10/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/LPBDTaylorSwiftBNPrizePackBeautyShot.png',
    "alt": "Win A Taylor Swift Guitar™ Little People, Big Dreams Library! Books include noted persons like Bruce Lee, Beyonce, and Martin Luther King Jr.",
    "defaultImagePath": "/content/dam/ccr/Sweepstakes/2024/03/LPBDTaylorSwiftBNPrizePackBeautyShot.png",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/LPBDTaylorSwiftBNPrizePackBeautyShot.png",
    "displayAlt": "Win A Taylor Swift Guitar™ Little People, Big Dreams Library! Books include noted persons like Bruce Lee, Beyonce, and Martin Luther King Jr."},
    
    
    
    {
    "count": "24",
    "workid": "1144221077",
    "headerMain": "Sweepstakes",
    "title": "&quot;The Comfort of Ghosts&quot; by Jacqueline Winspear Sweepstakes",
    "copy": "Pre-order <em>The Comfort of Ghosts</em> to be automatically entered for a chance to win a pottery mug, a Jo Malone candle, a Lambswool blanket, a $50 Barnes & Noble gift card and a signed copy of the book. The sweepstakes ends June 3, 2024.",
    "detailsCta":"See details and official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/the-comfort-of-ghosts-sweeps-rules.use.html",
    "startDate": "03/08/2024",
    "endDate": "06/03/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "25",
    "workid": "1144894254",
    "headerMain": "Sweepstakes",
    "title": "&quot;The Boyfriend&quot; by Freida McFadden Sweepstakes",
    "copy": "Pre-order <em>The Boyfriend</em> for a chance to win a $100 Barnes & Noble gift card, a luxe picnic basket, a murder mystery game and more! The sweepstakes ends on September 30.",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/the-boyfriend-sweeps-rules.use.html",
    "startDate": "03/08/2024",
    "endDate": "09/30/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "26",
    "workid": "1143886363",
    "headerMain": "Sweepstakes",
    "title": "&quot;Wisteria&quot; by Adalyn Grace Sweepstakes",
    "copy": "Pre-order <em>Wisteria</em> for a chance to win a $100 Barnes & Noble gift card, Wisteria Blue eau de parfum, a Little Bird sweatshirt and more! ",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/wisteria-by-adalyn-grace-sweepstakes.use.html",
    "startDate": "03/22/2024",
    "endDate": "08/19/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"},
    
    
    
    {
    "count": "27",
    "workid": "1144172649",
    "headerMain": "Sweepstakes",
    "title": "&quotSuch Charming Liars&quot by Karen McManus Sweepstakes",
    "copy": "Pre-order <em>Such Charming Liars</em> for a chance to win a $150 Barnes & Noble gift card, a ruby Mejuri necklace and a signed copy of the book! ",
    "detailsCta":"For more details and a full list of prizes, read the official rules here.",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2023/11/such-charming-liars-sweepstakes.use.html",
    "startDate": "03/22/2024",
    "endDate": "07/29/2024",
    "imagePath": '/content/dam/ccr/Sweepstakes/2024/03/SuchCharming_BN_Sweeps_Products.jpg',
    "alt": "Book Such Charming Liars, B&N Gift Card, and Gold Necklace",
    "defaultImagePath": "/content/dam/ccr/Sweepstakes/2024/03/SuchCharming_BN_Sweeps_Products.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/Sweepstakes/2024/03/SuchCharming_BN_Sweeps_Products.jpg",
    "displayAlt": "Book Such Charming Liars, B&N Gift Card, and Gold Necklace"},
    
    
    
    {
    "count": "28",
    "workid": "1144492833",
    "headerMain": "Sweepstakes",
    "title": "&quot;The Black Bird Oracle&quot; by Deborah Harkness Sweepstakes",
    "copy": "Pre-order <em>The Black Bird Oracle</em> to be automatically entered for a chance to win signed hardcover copies of Deborah Harkness books, All Souls Tea, a black bird tea towel and teapot. The sweepstakes ends July 15th, 2024.",
    "detailsCta":"See details and official rules here.   ",
    "detailsUrl": "https://dispatch.barnesandnoble.com/content/ccr/terms/details/2024/3/the-black-bird-oracle-sweeps-rules.use.html",
    "startDate": "03/27/2024",
    "endDate": "07/15/2024",
    "imagePath": '',
    "alt": "",
    "defaultImagePath": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "defaultImageAlt": "Sweepstakes Offers at Barnes & Noble",
    "displayImage": "/content/dam/ccr/global/misc/sweepstakes/default.jpg",
    "displayAlt": "Sweepstakes Offers at Barnes & Noble"}
    ];
    let pdpWorkID = window.location.pathname.split('/')[3];
    window.determineSweepsData = () => {
    var datum = "";
    window.sweepsData.forEach(dat => {
    var sweepEnd = new Date(dat.endDate);
    if(sweepEnd){sweepEnd=sweepEnd.setHours(23,59,58,0); }
    if( (!dat.endDate || sweepEnd > todaysDate) && (!dat.startDate || new Date(dat.startDate) <= todayOrPreviewDate ) ){
    if( dat.workid && dat.workid.length > 0 && pdpWorkID ){
    // if (dat.workid === pdpWorkID){ datum = dat; }
    if( dat.workid.match(new RegExp("(?:^|,)"+pdpWorkID+"(?:,|$)"))) {
    datum = dat;
    }
    }
    }
    });
    if(datum) {
    return datum;
    }else{
    return null;
    }
    };
    var data = window.determineSweepsData();
    if(data) {
    let greyBox = "//img.images-bn.com/static/redesign/srcs/images/grey-box.png";
    var theSweep = `<div class="sweep-stake-heading"><div class="bn-sweep-stake">`+data.headerMain+`</div></div><div class="sweepStake-content"><div class="sweep-stake-img "><img src="`+greyBox+`" data-resolvesrc="//dispatch.barnesandnoble.com`+data.displayImage +`" alt="`+data.displayAlt +`" class="Resolve lp-lazy" id="sweepstakes-image"></div><div class="sweepStake-right-content"><div class="sweepStake-title">`+data.title +`</div><div class="sweepStake-desc"><p>`+data.copy +`</p></div><p class="sweepStake-end-date">Ends `+data.endDate +`</p><p><a class="sweepStake-terms" data-modal-class="BN.Modal.External.Link" data-modal-scrolling="yes" data-modal-title="Sweepstakes Details" href="`+data.detailsUrl+`" target="_blank" onclick="set_cookie('pdp_sweepstakes_see-details_text');">`+data.detailsCta+`</a></p></div></div><hr class="mb-lg-s mt-0">`;
    $('#pdp-sweepstakes .sweep-stake-main-container').append(theSweep);
    }else{
    $('#pdp-sweepstakes .sweep-stake-main-container').append(`<div class="hidden sweepstakes-item not-available"></div>`);
    };
    }());
                </script>
    </div>
    <script src="//js.js-bn.com/static/redesign/release/js/blogs.js?v11.4.4">
    </script>
    <section class="container container--no-padding-bottom float-left pl-0 pr-0" id="blogsContainer">
    <!-- HTML Design -->
    <div class="blogs-main-container custom-blog-container">
    <div class="blog-heading">
    <div class="bn-blog">
                   From the B&amp;N Reads Blog
                  </div>
    <div class="responsive-carousel blog-pagination d-sm-none d-lg-block">
    <div class="slider-count">
                    Page
                    <span id="current">
                     1
                    </span>
                    of
                    <span id="total">
    </span>
    </div>
    </div>
    </div>
    <div class="blog-content product-shelf responsive-carousel" data-modifyslick="" data-slick="{'accessibility':false}" id="blog-carousel">
    </div>
    </div>
    <div class="clear">
    </div>
    <!-- HTML Design -->
    </section>
    <div class="clear">
    </div>
    <div class="related-subjects-section mb-s">
    <h2 class="mb-s related-subjects-section-title ml-sm-m ml-md-m">
                 Related Subjects
                </h2>
    <div class="d-flex related-subject-container-mobile">
    <div class="mb-s mr-s related-sub-fill-mobile cell1" id="related-sub-1">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/science-fiction-fantasy/_/N-8q8Z180l;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction &amp; Fantasy_text');">
                     Science Fiction &amp; Fantasy
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="mb-s mr-s related-sub-fill-mobile cell1" id="related-sub-2">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/science-fiction-fantasy/social-science-fiction/_/N-8q8Z1815;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Social Science Fiction_text');">
                     Social Science Fiction
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="mb-s mr-s related-sub-fill-mobile cell1" id="related-sub-3">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/_/N-181tZ8q8;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_High Tech and Hard Science Fiction_text');">
                     High Tech and Hard Science Fiction
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="mb-s mr-s related-sub-fill-mobile cell2" id="related-sub-4">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/_/N-181gZ8q8;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Space Exploration - Fiction_text');">
                     Space Exploration - Fiction
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="mb-s mr-s related-sub-fill-mobile cell2" id="related-sub-5">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/social-science-fiction/science-fiction-ecological/_/N-8q8Z181c;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Ecological_text');">
                     Science Fiction - Ecological
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="mb-s mr-s related-sub-fill-mobile cell2cell3" id="related-sub-6">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/social-science-fiction/science-fiction-science-religion/_/N-8q8Z1817;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Science &amp; Religion_text');">
                     Science Fiction - Science &amp; Religion
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="mb-s mr-s related-sub-fill-mobile cell3" id="related-sub-7">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/social-science-fiction/science-fiction-societies-cultures/_/N-8q8Z181e;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Societies &amp; Cultures_text');">
                     Science Fiction - Societies &amp; Cultures
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="mb-s mr-s related-sub-fill-mobile cell3" id="related-sub-8">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/mobile/b/books/social-science-fiction/science-fiction-strange-alien-worlds/_/N-8q8Z181a;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Strange &amp; Alien Worlds_text');">
                     Science Fiction - Strange &amp; Alien Worlds
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    </div>
    <div class="row related-subject-container">
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-0">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/science-fiction-fantasy/_/N-8q8Z180l;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction &amp; Fantasy_text');">
                     Science Fiction &amp; Fantasy
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-1">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/science-fiction-fantasy/social-science-fiction/_/N-8q8Z1815;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Social Science Fiction_text');">
                     Social Science Fiction
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-2">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/_/N-181tZ8q8;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_High Tech and Hard Science Fiction_text');">
                     High Tech and Hard Science Fiction
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-3">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/_/N-181gZ8q8;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Space Exploration - Fiction_text');">
                     Space Exploration - Fiction
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-4">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/social-science-fiction/science-fiction-ecological/_/N-8q8Z181c;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Ecological_text');">
                     Science Fiction - Ecological
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-5">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/social-science-fiction/science-fiction-science-religion/_/N-8q8Z1817;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Science &amp; Religion_text');">
                     Science Fiction - Science &amp; Religion
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-6">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/social-science-fiction/science-fiction-societies-cultures/_/N-8q8Z181e;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Societies &amp; Cultures_text');">
                     Science Fiction - Societies &amp; Cultures
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    <div class="col-lg-3 col-md-3 mb-s related-sub-fill" id="related-sub-7">
    <div class="related-sub-cell d-flex justify-content-between pl-xs pr-xs pt-xxs">
    <span class="related-sub-text pt-xxs">
    <a href="/b/books/social-science-fiction/science-fiction-strange-alien-worlds/_/N-8q8Z181a;jsessionid=59A4A13ADB80E3C95F91B52C84746CC6.prodny_store02-atgap04" onclick="set_cookie('trct_Related Categories_Science Fiction - Strange &amp; Alien Worlds_text');">
                     Science Fiction - Strange &amp; Alien Worlds
                    </a>
    </span>
    <span class="next-arrow-symbol pt-xxs ml-s">
    </span>
    </div>
    </div>
    </div>
    </div>
    <div class="container row editorial-reviews mt-m" id="EditorialReviews">
    <div class="col-lg-2">
    <div>
    </div>
    </div>
    <div class="col-lg-8">
    <aside>
    <h2 class="pb-sm-s pb-md-s">
                   Editorial Reviews
                  </h2>
    <blockquote>
    <p>
    <b>
                     Praise for
                     <i>
                      Dune
                     </i>
    </b>
    <br/>
    <br/>
                    “I know nothing comparable to it except
                    <i>
                     The Lord of the Rings
                    </i>
                    .”—Arthur C. Clarke
                    <br/>
    <br/>
                    “It is possible that
                    <i>
                     Dune
                    </i>
                    is even more relevant now than when it was first published.”—
                    <i>
                     The New Yorker
                    </i>
    <br/>
    <br/>
                    “An astonishing science fiction phenomenon.”—
                    <i>
                     The Washington Post
                    </i>
    <br/>
    <br/>
                    “One of the monuments of modern science fiction.”—
                    <i>
                     Chicago Tribune
                    </i>
    <br/>
    <br/>
                    “Powerful, convincing, and most ingenious.”—Robert A. Heinlein
                    <br/>
    <br/>
                    “Herbert’s creation of this universe, with its intricate development and analysis of ecology, religion, politics and philosophy, remains one of the supreme and seminal achievements in science fiction.”—
                    <i>
                     Louisville Times
                    </i>
    </p>
    <footer>
    <cite>
                     From the Publisher
                    </cite>
    </footer>
    </blockquote>
    </aside>
    </div>
    <div class="col-lg-2">
    <div>
    </div>
    </div>
    </div>
    <!-- Gigya Changes -->
    <!-- Gigya Changes -->
    <section class="pdp-page container" id="reviews">
    <h2 class="rule mb-l">
                 Customer Reviews
                </h2>
    <section class="customer-reviews-body" id="reviews-container">
    <div class="row">
    <div data-bv-product-id="9780593201893" data-bv-show="review_highlights">
    </div>
    </div>
    <div class="row">
    <div class="col-lg-12">
    <div data-bv-product-id="9780593201893" data-bv-show="reviews" id="reviews-list">
    </div>
    </div>
    </div>
    <div class="row">
    <div data-bv-product-id="9780593201893" data-bv-show="questions">
    </div>
    </div>
    </section>
    </section>
    <script defer="">
                $(function() {
    var isLoggedIn = false;
    var ratingsParams = {
    categoryID: 'Products',
    streamID: '1136810577', /* use Product ID for unique identifier? SkuID? - prd9780593201893 - ProductID? */
    containerID: 'ratingsDisplay',
    width: '100%',
    showCommentButton: false,
    ratingTemplate: '<span id="avgRating" class="hidden" tabindex="0"></span><span id="read-stars" class="gig-rating-stars" role="img"></span><a href="#" class="gig-rating-readReviewsLink" aria-describedby="read-stars"></a>',
    onReadReviewsClicked: gotoReviews,
    onLoad: function() {
    var $reviewLink = $('.gig-rating-readReviewsLink','#ratingsDisplay'),
    // numRating = $(".gig-average-review").html();
    //SRL-2749
    numRating = $('.gig-rating-stars').attr('title') || $(".gig-average-review").html() || 0;
    var skutype = 'book',
    $headerReviewLink = $('.sticky-left .gig-rating-readReviewsLink'),
    reviewCountTxt = $reviewLink.html();
    if($reviewLink.html() === "0 Reviews") {
    $reviewLink.html("Be the first to write a review");
    }
    else if(skutype == 'book' || skutype == 'eBook'){
    if($reviewLink.html() === "1 Review"){
    reviewCountTxt = reviewCountTxt.replace("Review", "Customer Review");
    }
    else{
    reviewCountTxt = reviewCountTxt.replace("Reviews", "Customer Reviews");
    }
    $headerReviewLink.html(reviewCountTxt);
    }
    var widthOfAuthor= calculateWidthOfauthor();
    var widthOfReadReviewsLink= parseInt($('.header-gigiya-wrapper .gig-rating-readReviewsLink').width());
    if($('.read-review-header').length)	{
    $('.read-review-header').removeClass('hidden');
    $('.header-gigiya-wrapper .header-gigiya-inner').width(250 + widthOfAuthor + widthOfReadReviewsLink );
    }
    if($('#EditorialReviews').length){
    $('.editorial-review-header').removeClass('hidden');
    $('.header-gigiya-wrapper .header-gigiya-inner').width(250 + widthOfAuthor + widthOfReadReviewsLink );
    }
    $("#avgRating").html("Average Rating: " + numRating);
    //SRL-2749 : Star rating information is not clear
    var ariaText = numRating + " rating out of 5 Stars";
    $(".gig-rating-stars").attr('aria-label',ariaText);
    initBuyOptnsPDP();
    }
    },
    ratingsParamsComments = {
    categoryID: 'Products',
    streamID: '1136810577',
    containerID: 'prodReviewInfo',
    ratingTemplate:
    '<div class="gig-rating-stars"></div>' +
    '<p><a href="/reviews/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893" class="gig-rating-readReviewsLink" aria-describedby="read-stars"></a></p>',
    width: '100%',
    showCommentButton: false,
    onReadReviewsClicked: gotoReviews,
    onLoad: function() {
    var $reviewLink = $('.gig-rating-readReviewsLink','#prodReviewInfo'),
    numRating = $('#ratingsDisplay .gig-rating-stars').attr('title') || $(".gig-average-review").first().text() || 0;
    if ($reviewLink.html() === "0 Reviews") {
    $reviewLink.html("Be the first to write a review");
    $('.customer-reviews-body h3').hide();
    $('.reviews-view-all').hide();
    $('.customer-reviews-body').append('<hr class="mt-0 mb-0" />');
    }
    
    // Analytics set review and ratings
    if(typeof s_setP !== 'undefined' && typeof s_getP !== 'undefined') {
    var digitalDataRating = s_getP('digitalData.product[0].attributes.rating'),
    digitalDataReview = s_getP('digitalData.product[0].attributes.reviews'),
    numReview = 0,
    $review = $('.gig-rating-readReviewsLink').first(),
    reviewStringParse = '';
    if($review.length > 0) {
    reviewStringParse = $review.text();
    numReview = reviewStringParse.replace(/reviews/gi,'').trim();
    }
    if(typeof digitalDataRating == 'undefined' || digitalDataRating != numRating) {
    s_setP('digitalData.product[0].attributes.rating', parseFloat(numRating));
    }
    
    if((typeof digitalDataReview == 'undefined' || digitalDataReview != numReview) && !isNaN(numReview)) {
    s_setP('digitalData.product[0].attributes.reviews', parseInt(numReview, 10));
    }
    
    }
    // Gigya ratings and reviews loads after document is ready,
    // so direct call needs to called onload instead
    $(document).trigger('analytics-track-pdp');
    }
    },
    params = {
    categoryID: "Products",
    streamID: "1136810577",
    callback:updateDOM
    },
    commentParams = {
    version:2,
    sort: 'votesDesc',
    threaded: true,
    
    threadLimit: 3,
    
    categoryID: 'Products',
    streamID: '1136810577',
    containerID: 'reviews-list',
    width: '100%',
    useSiteLogin: true,
    onLoad: function() {
    if(typeof performance.mark !== 'undefined' && typeof performance.measure !== 'undefined')
    {
    performance.mark("Customer_Reviews_Gigya_loading_ends");
    performance.measure(
    "customerReviewsDur",
    "Customer_Reviews_Gigya_loading_starts",
    "Customer_Reviews_Gigya_loading_ends"
    );
    }
    //ATG-23455 : remove fixed height for the comments container
    $('.gig-comments-more').on('click', function(){
    $('#reviews-list').css('height','100%');
    });
    //SRL-2731
    $('div.gig-simpleShareUI-button').each(function(){
    var ariaTitle = $(this).find('.gig-simpleShareUI-buttonText').text();
    $(this).children('.gig-simpleShareUI-button-inner').attr({
    role:'button',
    title : ariaTitle
    });
    });
    $('.gig-simpleShareUI-closeButton').attr('role', 'button');
    $('.gig-simpleShareUI-closeButton').attr('title','Close');
    //SRL-2731 ends
    //ATG-19340 starts
    var adColumnHeight = $('#adcontainer1').outerHeight(true);
    if(adColumnHeight<19){
    $('.customer-reviews-body').css({'min-height': "0px"});
    }
    //ATG-19772 starts : to set min-height for mouse hover in customer-reviews
    else{
    $('.customer-reviews-body').css({'min-height': "300px"});
    }
    //ATG-19772 ends
    //ATG-19340 ends
    //ADA SRL-2382
    $('.gig-comment-shareLink').each(function(){
    $(this).attr({
    role:'link',
    tabindex:'0',
    });
    var triggerEle = $(this);
    var focusPlaced = function(){
    $('.gig-simpleShareUI-closeButton').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-closeButton').focus();
    $('.gig-simpleShareUI-closeButton').on('keydown click',function(e){
    if(e.keyCode === 13){
    $(this).trigger('click');
    $(triggerEle).focus();
    }
    else if(e.shiftKey && e.keyCode==9){
    $('.gig-simpleShareUI-buttonText-more').focus();
    e.preventDefault();
    }
    else if(e.type == 'click'){
    $(triggerEle).focus();
    }
    });
    $('.gig-simpleShareUI-buttonText-facebook').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-email').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-twitter').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-googleplus').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-messenger').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-linkedin').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-digg').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-delicious').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-stumbleupon').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-hyves').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-baidu').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-more').attr({
    'tabindex' : '0',
    'role' : 'link'
    });
    $('.gig-simpleShareUI-buttonText-facebook').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-email').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-twitter').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-googleplus').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-messenger').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-linkedin').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-digg').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-delicious').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-stumbleupon').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-hyves').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    $('.gig-simpleShareUI-buttonText-baidu').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    var socialModalFocus = function(){
    $('img[style="cursor:pointer;"]:first').attr({
    'tabindex' : '0',
    'role' : 'button',
    'aria-label' : 'Close'
    });
    $("img[id$='arrow_left']").attr({
    'tabindex' : '0',
    'role' : 'button',
    'aria-label' : 'Previous'
    });
    $("img[id$='arrow_right']").attr({
    'tabindex' : '0',
    'role' : 'button',
    'aria-label' : 'Next'
    });
    $("img[id$='arrow_right_disable']").attr({
    'tabindex' : '0',
    'role' : 'button',
    'aria-label' : 'Next Disabled'
    });
    $("img[id$='arrow_left_disable']").attr({
    'tabindex' : '0',
    'role' : 'button',
    'aria-label' : 'Previous Disabled'
    });
    $('img[style="cursor:pointer;"]:first').focus();
    $('img[style="cursor:pointer;"]:first').on('keydown click',function(e){
    var triggerElement = $(this);
    if(e.keyCode==13){
    $(this).trigger('click');
    $(triggerEle).focus();
    }
    else if(e.type == 'click'){
    $(triggerEle).focus();
    }
    });
    $("img[id$='arrow_right']").on('keydown',function(e){
    if((!e.shiftKey && e.keyCode==9) || e.keyCode==13){
    $(this).trigger('click');
    setTimeout(function(){
    $('.tabbing-button:visible:first').focus();
    },0);
    }
    });
    $("img[id$='arrow_right_disable']").on('keydown',function(e){
    if(!e.shiftKey && e.keyCode==9){
    $('img[style="cursor:pointer;"]:first').focus();
    e.preventDefault();
    }
    });
    $("img[id$='arrow_left']").on('keydown',function(e){
    if((e.shiftKey && e.keyCode==9) || e.keyCode==13){
    $(this).trigger('click');
    setTimeout(function(){
    $('.tabbing-button:visible:last').focus();
    },0);
    }
    });
    $("img[id$='arrow_left_disable']").on('keydown',function(e){
    if(e.shiftKey && e.keyCode==9){
    $('img[style="cursor:pointer;"]:first').focus();
    e.preventDefault();
    }
    });
    $('img[style="cursor:pointer;"]:first').on('keydown',function(e){
    if(e.shiftKey && e.keyCode==9){
    if($("img[id$='arrow_right']").is(':visible')){
    $("img[id$='arrow_right']").focus();
    e.preventDefault();
    }
    else
    $('img[id$="arrow_right_disable"]').focus();
    e.preventDefault();
    }
    });
    $("[id$='_showShareUI_bookmarksWidget_page']").find("table").each(function(){
    $(this).find("tr").each(function(){
    if($(this).find("table").length > 0){
    $(this).find("table").each(function(){
    $(this).find("td").each(function(){
    var title = $(this).find("div").attr("title");
    $(this).find("div").find("button").attr("aria-label",title);
    });
    });
    }
    });
    });
    }
    $('.gig-simpleShareUI-buttonText-more').on('keydown click',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    var check = setInterval(function(){
    if($("img[id$='arrow_left']").length > 0){
    socialModalFocus();
    clearInterval(check);
    }
    },200);
    }
    else if(!e.shiftKey && e.keyCode==9){
    $('.gig-simpleShareUI-closeButton').focus();
    e.preventDefault();
    }
    else if(e.type == 'click'){
    var check = setInterval(function(){
    if($("img[id$='arrow_left']").length > 0){
    socialModalFocus();
    clearInterval(check);
    }
    },200);
    }
    });
    }
    $(this).on('keydown click',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    var check = setInterval(function(){
    if($('.gig-simpleShareUI-closeButton').length > 0){
    focusPlaced();
    clearInterval(check);
    }
    },200);
    }
    else if(e.type == 'click'){
    var check = setInterval(function(){
    if($('.gig-simpleShareUI-closeButton').length > 0){
    focusPlaced();
    clearInterval(check);
    }
    },200);
    }
    });
    });
    $('.gig-comment-flag').each(function(){
    var target=$(this);
    $(this).attr({
    role:'link',
    tabindex:'0',
    });
    var focusGiven = function(){
    $('.gig-comments-dialog-close').attr({
    'tabindex' : '0',
    'role' : 'button',
    'title' : 'Close'
    });
    $('.gig-comments-dialog-button-ok').attr({
    'tabindex' : '0',
    'role' : 'button'
    });
    $('.gig-comments-dialog-button-cancel').attr({
    'tabindex' : '0',
    'role' : 'button'
    });
    $('.gig-comments-dialog-close').focus();
    $('.gig-comments-dialog-close').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    $(target).focus();
    }
    else if(e.shiftKey && e.keyCode==9){
    $(this).parents('.gig-comments-dialog').find('.gig-comments-dialog-button-cancel').focus();
    e.preventDefault();
    }
    });
    $('.gig-comments-dialog-button-cancel').on('keydown',function(e){
    if(!e.shiftKey && e.keyCode==9){
    $(this).parents('.gig-comments-dialog').find('.gig-comments-dialog-close').focus();
    e.preventDefault();
    }
    else if(e.shiftKey && e.keyCode==9){
    $(this).parents('.gig-comments-dialog').find('.gig-comments-dialog-button-ok').focus();
    e.preventDefault();
    }
    else if(e.keyCode==13){
    $(this).trigger('click');
    $(target).focus();
    }
    });
    $('.gig-comments-dialog-button-ok').on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    else if(e.shiftKey && e.keyCode==9){
    $(this).parents('.gig-comments-dialog').find('.gig-comments-dialog-close').focus();
    e.preventDefault();
    }
    });
    }
    $(this).attr('tabindex','0');
    $(this).on('keydown click',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    focusGiven();
    }
    else if(e.type == 'click'){
    focusGiven();
    }
    });
    });
    $('.gig-comment-vote-pos').each(function(){
    $(this).attr({
    role:'button',
    tabindex:'0',
    });
    $(this).on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    });
    $('.gig-comment-vote-neg').each(function(){
    $(this).attr({
    role:'button',
    tabindex:'0',
    });
    $(this).on('keydown',function(e){
    if(e.keyCode==13){
    $(this).trigger('click');
    }
    });
    });
    $('.gig-comment-content').each(function(){
    $(this).attr('tabindex','0');
    });
    //ADA SRL-2382 ends
    var reviewsContainer = $('#reviews-container');
    var commentsContainer = $('.gig-comments-comments');
    var pos = $('.gig-comment-vote-pos');
    var neg = $('.gig-comment-vote-neg');
    if (commentsContainer.is(':empty')) {
    return;
    } else {
    reviewsContainer.removeClass('hidden');
    }
    if (!isLoggedIn) {
    pos.addClass('sign-in-link');
    neg.addClass('sign-in-link');
    }
    /* SRL-461 : Providing suitable aria-label for the Like and Diskike button in Customer Reviews */
    $(".gig-comment-self-data").each(function(i) {
    var like = $(this).find('.gig-comment-vote-pos').html() + " people like this review." ;
    var dislike = $(this).find('.gig-comment-vote-neg').html() + " people dislike this review." ;
    $(this).find('.gig-comment-vote-pos').attr('aria-label',like);
    $(this).find('.gig-comment-vote-neg').attr('aria-label',dislike);
    });
    $(".gig-comment-title").each(function(index) {
    var count = $(this).find(".gig-comment-rating-star-full").length;
    var maxCount = $(this).find(".gig-comment-rating-star").length;
    var reviewRating = "This review rates " + count + " out of " + maxCount + " stars.";
    $(this).prepend('<span id="userRating' + index + '" class="hidden" style="display:none;">Rating: ' + count + ' out of '+ maxCount + '</span>');
    $(this).find(".gig-comment-rating").attr({"aria-label":reviewRating , "role":"img" , "title":count , "alt":count});
    });
    }
    };
    function updateDOM(response) {
    var overallRating = response.streamInfo.avgRatings._overall;
    if ( response.errorCode == 0 ) {
    $(".gig-average-review").html(overallRating);
    }
    }
    function gotoReviews(eventObj) {
    var skutype = 'book',
    $reviewLink = $('.gig-rating-readReviewsLink'),
    reviewLocation = eventObj && eventObj.instanceID ? eventObj.instanceID : '',
    setLocation = (reviewLocation === 'ratingsDisplay') ? 'topOfPage' : 'customerReviewsBox';
    $(document).triggerHandler('analytics-reviews-clicked', {location: setLocation});
    if ($reviewLink.html() === "Be the first to write a review") {
    $("#writeReviewBtn").click();
    } else {
    if(skutype == 'book' || skutype == 'eBook'){
    document.getElementById('reviews').scrollIntoView();
    } else {
    window.location = "/reviews/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893#reviews-header";
    }
    }
    }
    if(typeof gigya != 'undefined') {
    if(typeof performance.mark !== 'undefined')
    {
    performance.mark("Customer_Reviews_Gigya_loading_starts");
    }
    // gigya.comments.getStreamInfo(params);
    // gigya.comments.showRatingUI(ratingsParams);
    //gigya.comments.showRatingUI(ratingsParamsComments);
    //gigya.comments.showCommentsUI(commentParams);
    }
    });
    function calculateWidthOfauthor(){
    var widthAuthor= 0;
    if($(".header-gigiya-wrapper .sticky-author .contributors").find("a").length > 0){
    $('.header-gigiya-wrapper .sticky-author .contributors  a').each(function(){
    widthAuthor += parseFloat($(this).width())+ 12;
    });
    }
    else{
    widthAuthor += $(".header-gigiya-wrapper .sticky-author .contributors").width();
    }
    if($('.header-gigiya-wrapper .sticky-author .contributors').text().indexOf('Director')>-1){
    widthAuthor +=45;
    }
    if($('.header-gigiya-wrapper .sticky-author .contributors').text().indexOf('Cast')>-1){
    widthAuthor +=25;
    }
    if($('.header-gigiya-wrapper .sticky-author .contributors').text().indexOf('by')>-1){
    widthAuthor +=15;
    }
    return widthAuthor;
    }
               </script>
    <section class="mt-m text--center" data-carousel-type="book-carousel" data-slick='{"accessibility":false}' id="recentlyViewed">
    <div class="mini-cart-spinner">
    </div>
    </section>
    <!-- Internal Component Tracking - Begin -->
    <!-- Internal Component Tracking - End -->
    <script>
                if(typeof performance.mark !== 'undefined')
    performance.mark("BloomReach_Widget_loading_starts");
               </script>
    <script src="//js.js-bn.com/static/redesign/release/js/bloomreach.js?v11.4.4">
    </script>
    <div class="container container--no-padding-bottom d-none" id="bloomReachContainer">
    <!-- Related Searches -->
    <div class="d-none" id="relatedSearchesContainer">
    <div class="row">
    <div class="col-lg-12 col-md-12 col-sm-12">
    <div id="bloomReachRelatedSearch">
    <section class="book bloomReachRelatedSearch" data-modifyslick="">
    <header class="one-col-crsl-header">
    <h2 class="float-left">
                       Related Searches
                      </h2>
    <div class="clear">
    </div>
    </header>
    <div class="product-shelf responsive-carousel" data-responsive-carousel='{"slidesToShow": "5", "slidesToScroll": "5", "adaptiveHeight": false, "infinite": false, "accessibility": false, "focusOnChange": false, "focusOnSelect": false}'>
    <div class="product-shelf-tile">
    <div class="text-center">
    <div class="related-search-rectangle">
    <div>
    <svg alt="search" class="brand float-left" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
    <path d="M7.886 13.54c3.266 0 5.914-2.54 5.914-5.672 0-3.134-2.648-5.673-5.914-5.673-3.266 0-5.914 2.54-5.914 5.673.007 3.13 2.65 5.665 5.913 5.672h.001zM0 7.867v-.011C0 3.679 3.53.29 7.886.29c4.355 0 7.885 3.388 7.885 7.565a7.34 7.34 0 01-1.668 4.654l6.584 6.287a.923.923 0 01.313.692c0 .522-.441.945-.986.945-.283 0-.54-.115-.72-.3l-6.572-6.305a8.047 8.047 0 01-4.836 1.59C3.535 15.42.007 12.04 0 7.868v-.001z" fill="#828c8e" fill-rule="evenodd">
    </path>
    </svg>
    </div>
    <a class="product-shelf-author related-search-title" href="/b/series/dune-chronicles-series/_/N-2kpe" onclick="set_cookie('emirs_Dune Chronicles Series_na_text');" title="Frank Herbert's Dune series is one of the grandest epics in imaginative literature. Set in the distant future and taking place over millennia, the books deal with themes such as human survival, evolution, and power.">
                          Dune Chronicles Series
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile">
    <div class="text-center">
    <div class="related-search-rectangle">
    <div>
    <svg alt="search" class="brand float-left" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
    <path d="M7.886 13.54c3.266 0 5.914-2.54 5.914-5.672 0-3.134-2.648-5.673-5.914-5.673-3.266 0-5.914 2.54-5.914 5.673.007 3.13 2.65 5.665 5.913 5.672h.001zM0 7.867v-.011C0 3.679 3.53.29 7.886.29c4.355 0 7.885 3.388 7.885 7.565a7.34 7.34 0 01-1.668 4.654l6.584 6.287a.923.923 0 01.313.692c0 .522-.441.945-.986.945-.283 0-.54-.115-.72-.3l-6.572-6.305a8.047 8.047 0 01-4.836 1.59C3.535 15.42.007 12.04 0 7.868v-.001z" fill="#828c8e" fill-rule="evenodd">
    </path>
    </svg>
    </div>
    <a class="product-shelf-author related-search-title" href="/b/contributor/frank-herbert-/_/N-2k97" onclick="set_cookie('emirs_Frank Herbert_na_text');" title="Herbert didn't invent ecological sci-fi, but he made it famous with &lt;em&gt;Dune&lt;/em&gt;.">
                          Frank Herbert
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile">
    <div class="text-center">
    <div class="related-search-rectangle">
    <div>
    <svg alt="search" class="brand float-left" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
    <path d="M7.886 13.54c3.266 0 5.914-2.54 5.914-5.672 0-3.134-2.648-5.673-5.914-5.673-3.266 0-5.914 2.54-5.914 5.673.007 3.13 2.65 5.665 5.913 5.672h.001zM0 7.867v-.011C0 3.679 3.53.29 7.886.29c4.355 0 7.885 3.388 7.885 7.565a7.34 7.34 0 01-1.668 4.654l6.584 6.287a.923.923 0 01.313.692c0 .522-.441.945-.986.945-.283 0-.54-.115-.72-.3l-6.572-6.305a8.047 8.047 0 01-4.836 1.59C3.535 15.42.007 12.04 0 7.868v-.001z" fill="#828c8e" fill-rule="evenodd">
    </path>
    </svg>
    </div>
    <a class="product-shelf-author related-search-title" href="/w/brave-new-world/aldous-huxley/1100158848" onclick="set_cookie('emirs_Brave New World_na_text');" title="Brave New World">
                          Brave New World
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile">
    <div class="text-center">
    <div class="related-search-rectangle">
    <div>
    <svg alt="search" class="brand float-left" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
    <path d="M7.886 13.54c3.266 0 5.914-2.54 5.914-5.672 0-3.134-2.648-5.673-5.914-5.673-3.266 0-5.914 2.54-5.914 5.673.007 3.13 2.65 5.665 5.913 5.672h.001zM0 7.867v-.011C0 3.679 3.53.29 7.886.29c4.355 0 7.885 3.388 7.885 7.565a7.34 7.34 0 01-1.668 4.654l6.584 6.287a.923.923 0 01.313.692c0 .522-.441.945-.986.945-.283 0-.54-.115-.72-.3l-6.572-6.305a8.047 8.047 0 01-4.836 1.59C3.535 15.42.007 12.04 0 7.868v-.001z" fill="#828c8e" fill-rule="evenodd">
    </path>
    </svg>
    </div>
    <a class="product-shelf-author related-search-title" href="/w/fahrenheit-451/ray-bradbury/1100383286" onclick="set_cookie('emirs_Fahrenheit 451: A Novel_na_text');" title="Fahrenheit 451: A Novel">
                          Fahrenheit 451: A Novel
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile">
    <div class="text-center">
    <div class="related-search-rectangle">
    <div>
    <svg alt="search" class="brand float-left" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
    <path d="M7.886 13.54c3.266 0 5.914-2.54 5.914-5.672 0-3.134-2.648-5.673-5.914-5.673-3.266 0-5.914 2.54-5.914 5.673.007 3.13 2.65 5.665 5.913 5.672h.001zM0 7.867v-.011C0 3.679 3.53.29 7.886.29c4.355 0 7.885 3.388 7.885 7.565a7.34 7.34 0 01-1.668 4.654l6.584 6.287a.923.923 0 01.313.692c0 .522-.441.945-.986.945-.283 0-.54-.115-.72-.3l-6.572-6.305a8.047 8.047 0 01-4.836 1.59C3.535 15.42.007 12.04 0 7.868v-.001z" fill="#828c8e" fill-rule="evenodd">
    </path>
    </svg>
    </div>
    <a class="product-shelf-author related-search-title" href="/w/red-rising/pierce-brown/1110614785" onclick="set_cookie('emirs_Red Rising (Red Rising Series #1)_na_text');" title="Red Rising (Red Rising Series #1)">
                          Red Rising (Red Rising Series #1)
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile">
    <div class="text-center">
    <div class="related-search-rectangle">
    <div>
    <svg alt="search" class="brand float-left" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
    <path d="M7.886 13.54c3.266 0 5.914-2.54 5.914-5.672 0-3.134-2.648-5.673-5.914-5.673-3.266 0-5.914 2.54-5.914 5.673.007 3.13 2.65 5.665 5.913 5.672h.001zM0 7.867v-.011C0 3.679 3.53.29 7.886.29c4.355 0 7.885 3.388 7.885 7.565a7.34 7.34 0 01-1.668 4.654l6.584 6.287a.923.923 0 01.313.692c0 .522-.441.945-.986.945-.283 0-.54-.115-.72-.3l-6.572-6.305a8.047 8.047 0 01-4.836 1.59C3.535 15.42.007 12.04 0 7.868v-.001z" fill="#828c8e" fill-rule="evenodd">
    </path>
    </svg>
    </div>
    <a class="product-shelf-author related-search-title" href="/w/golden-son/pierce-brown/1118476760" onclick="set_cookie('emirs_Golden Son (Red Rising Series #2)_na_text');" title="Golden Son (Red Rising Series #2)">
                          Golden Son (Red Rising Series #2)
                         </a>
    </div>
    </div>
    </div>
    </div>
    </section>
    </div>
    </div>
    </div>
    </div>
    <!-- Explore More Items -->
    <div class="d-none" id="exploreItemsContainer">
    <div class="row">
    <div class="col-lg-12 col-md-12 col-sm-12">
    <div id="bloomReachExploreItems">
    <section class="mb-5 book bloomReachExploreItems" data-modifyslick="">
    <header class="one-col-crsl-header">
    <h2 class="float-left">
                       Explore More Items
                      </h2>
    <div class="clear">
    </div>
    </header>
    <div class="product-shelf responsive-carousel" data-modifyslick="" data-responsive-carousel='{"slidesToShow": "4|4", "slidesToScroll": "4|4", "adaptiveHeight": false, "infinite": false}' data-slick="{'accessibility':false}" id="bloomreach-carousel">
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/dune-messiah/frank-herbert/1100316376" onclick="set_cookie('emi_/w/dune-messiah/frank-herbert/1100316376_na_image');" title="view details">
    <noscript>
    <img alt="Dune Messiah" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780593098233_p0_v1_s90x140.jpg" title="Dune Messiah"/>
    </noscript>
    <img alt="Dune Messiah" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780593098233_p0_v1]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/dune-messiah/frank-herbert/1100316376" onclick="set_cookie('emi_Dune Messiah_na_text');" title="Dune Messiah">
                          Dune Messiah
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-1">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780593098233" data-imgurl="prodimage.images-bn.com/pimages/9780593098233_p0_v1_s90x140.jpg" data-pdpurl="/w/dune-messiah/frank-herbert/1100316376" data-synopsis=" " data-title="Dune Messiah" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/children-of-dune/frank-herbert/1100361916" onclick="set_cookie('emi_/w/children-of-dune/frank-herbert/1100361916_na_image');" title="view details">
    <noscript>
    <img alt="Children of Dune" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780593098240_p0_v1_s90x140.jpg" title="Children of Dune"/>
    </noscript>
    <img alt="Children of Dune" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780593098240_p0_v1]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/children-of-dune/frank-herbert/1100361916" onclick="set_cookie('emi_Children of Dune_na_text');" title="Children of Dune">
                          Children of Dune
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-2">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780593098240" data-imgurl="prodimage.images-bn.com/pimages/9780593098240_p0_v1_s90x140.jpg" data-pdpurl="/w/children-of-dune/frank-herbert/1100361916" data-synopsis=" " data-title="Children of Dune" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/dune/frank-herbert/1100608835" onclick="set_cookie('emi_/w/dune/frank-herbert/1100608835_na_image');" title="view details">
    <noscript>
    <img alt="Dune (Movie Tie-In)" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780593438367_p0_v2_s90x140.jpg" title="Dune (Movie Tie-In)"/>
    </noscript>
    <img alt="Dune (Movie Tie-In)" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780593438367_p0_v2]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/dune/frank-herbert/1100608835" onclick="set_cookie('emi_Dune (Movie Tie-In)_na_text');" title="Dune (Movie Tie-In)">
                          Dune (Movie Tie-In)
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-3">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780593438367" data-imgurl="prodimage.images-bn.com/pimages/9780593438367_p0_v2_s90x140.jpg" data-pdpurl="/w/dune/frank-herbert/1100608835" data-synopsis=" " data-title="Dune (Movie Tie-In)" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/chapterhouse/frank-herbert/1100623316" onclick="set_cookie('emi_/w/chapterhouse/frank-herbert/1100623316_na_image');" title="view details">
    <noscript>
    <img alt="Chapterhouse: Dune" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780593201770_p0_v1_s90x140.jpg" title="Chapterhouse: Dune"/>
    </noscript>
    <img alt="Chapterhouse: Dune" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780593201770_p0_v1]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/chapterhouse/frank-herbert/1100623316" onclick="set_cookie('emi_Chapterhouse: Dune_na_text');" title="Chapterhouse: Dune">
                          Chapterhouse: Dune
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-4">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780593201770" data-imgurl="prodimage.images-bn.com/pimages/9780593201770_p0_v1_s90x140.jpg" data-pdpurl="/w/chapterhouse/frank-herbert/1100623316" data-synopsis=" " data-title="Chapterhouse: Dune" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/frank-herberts-dune-saga-6-book-boxed-set/frank-herbert/1136810574" onclick="set_cookie('emi_/w/frank-herberts-dune-saga-6-book-boxed-set/frank-herbert/1136810574_na_image');" title="view details">
    <noscript>
    <img alt="Frank Herbert's Dune Saga 6-Book Boxed Set: Dune, Dune Messiah, Children of Dune, God Emperor of Dune, Heretics of Dune, and Chapterhouse: Dune" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780593201886_p0_v4_s90x140.jpg" title="Frank Herbert's Dune Saga 6-Book Boxed Set: Dune, Dune Messiah, Children of Dune, God Emperor of Dune, Heretics of Dune, and Chapterhouse: Dune"/>
    </noscript>
    <img alt="Frank Herbert's Dune Saga 6-Book Boxed Set: Dune, Dune Messiah, Children of Dune, God Emperor of Dune, Heretics of Dune, and Chapterhouse: Dune" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780593201886_p0_v4]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/frank-herberts-dune-saga-6-book-boxed-set/frank-herbert/1136810574" onclick="set_cookie('emi_Frank Herbert's Dune Saga 6-Book Boxed Set: Dune, Dune Messiah, Children of Dune, God Emperor of Dune, Heretics of Dune, and Chapterhouse: Dune_na_text');" title="Frank Herbert's Dune Saga 6-Book Boxed Set: Dune, Dune Messiah, Children of Dune, God Emperor of Dune, Heretics of Dune, and Chapterhouse: Dune">
                          Frank Herbert's Dune Saga 6-Book Boxed Set: Dune, Dune Messiah, Children of Dune, God Emperor of Dune, Heretics of Dune, and Chapterhouse: Dune
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-5">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780593201886" data-imgurl="prodimage.images-bn.com/pimages/9780593201886_p0_v4_s90x140.jpg" data-pdpurl="/w/frank-herberts-dune-saga-6-book-boxed-set/frank-herbert/1136810574" data-synopsis=" " data-title="Frank Herbert's Dune Saga 6-Book Boxed Set: Dune, Dune Messiah, Children of Dune, God Emperor of Dune, Heretics of Dune, and Chapterhouse: Dune" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/hellstroms-hive/frank-herbert/1100351299" onclick="set_cookie('emi_/w/hellstroms-hive/frank-herbert/1100351299_na_image');" title="view details">
    <noscript>
    <img alt="Hellstrom's Hive" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780765317728_p0_v5_s90x140.jpg" title="Hellstrom's Hive"/>
    </noscript>
    <img alt="Hellstrom's Hive" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780765317728_p0_v5]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/hellstroms-hive/frank-herbert/1100351299" onclick="set_cookie('emi_Hellstrom's Hive_na_text');" title="Hellstrom's Hive">
                          Hellstrom's Hive
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-6">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780765317728" data-imgurl="prodimage.images-bn.com/pimages/9780765317728_p0_v5_s90x140.jpg" data-pdpurl="/w/hellstroms-hive/frank-herbert/1100351299" data-synopsis=" " data-title="Hellstrom's Hive" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/the-dosadi-experiment/frank-herbert/1102340725" onclick="set_cookie('emi_/w/the-dosadi-experiment/frank-herbert/1102340725_na_image');" title="view details">
    <noscript>
    <img alt="The Dosadi Experiment" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9781250163691_p0_v3_s90x140.jpg" title="The Dosadi Experiment"/>
    </noscript>
    <img alt="The Dosadi Experiment" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9781250163691_p0_v3]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/the-dosadi-experiment/frank-herbert/1102340725" onclick="set_cookie('emi_The Dosadi Experiment_na_text');" title="The Dosadi Experiment">
                          The Dosadi Experiment
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-7">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9781250163691" data-imgurl="prodimage.images-bn.com/pimages/9781250163691_p0_v3_s90x140.jpg" data-pdpurl="/w/the-dosadi-experiment/frank-herbert/1102340725" data-synopsis=" " data-title="The Dosadi Experiment" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/a-thorn-in-the-bush/frank-herbert/1120743863" onclick="set_cookie('emi_/w/a-thorn-in-the-bush/frank-herbert/1120743863_na_image');" title="view details">
    <noscript>
    <img alt="A Thorn in the Bush" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9781614752837_p0_v4_s90x140.jpg" title="A Thorn in the Bush"/>
    </noscript>
    <img alt="A Thorn in the Bush" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9781614752837_p0_v4]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/a-thorn-in-the-bush/frank-herbert/1120743863" onclick="set_cookie('emi_A Thorn in the Bush_na_text');" title="A Thorn in the Bush">
                          A Thorn in the Bush
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-8">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9781614752837" data-imgurl="prodimage.images-bn.com/pimages/9781614752837_p0_v4_s90x140.jpg" data-pdpurl="/w/a-thorn-in-the-bush/frank-herbert/1120743863" data-synopsis=" " data-title="A Thorn in the Bush" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/direct-descent/frank-herbert/1103565993" onclick="set_cookie('emi_/w/direct-descent/frank-herbert/1103565993_na_image');" title="view details">
    <noscript>
    <img alt="Direct Descent" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9781614752929_p0_v3_s90x140.jpg" title="Direct Descent"/>
    </noscript>
    <img alt="Direct Descent" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9781614752929_p0_v3]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/direct-descent/frank-herbert/1103565993" onclick="set_cookie('emi_Direct Descent_na_text');" title="Direct Descent">
                          Direct Descent
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-9">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9781614752929" data-imgurl="prodimage.images-bn.com/pimages/9781614752929_p0_v3_s90x140.jpg" data-pdpurl="/w/direct-descent/frank-herbert/1103565993" data-synopsis=" " data-title="Direct Descent" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/herejes-de-dune-heretics-of-dune/frank-herbert/1140077613" onclick="set_cookie('emi_/w/herejes-de-dune-heretics-of-dune/frank-herbert/1140077613_na_image');" title="view details">
    <noscript>
    <img alt="Herejes de Dune / Heretics of Dune" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9788466359399_p0_v1_s90x140.jpg" title="Herejes de Dune / Heretics of Dune"/>
    </noscript>
    <img alt="Herejes de Dune / Heretics of Dune" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9788466359399_p0_v1]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/herejes-de-dune-heretics-of-dune/frank-herbert/1140077613" onclick="set_cookie('emi_Herejes de Dune / Heretics of Dune_na_text');" title="Herejes de Dune / Heretics of Dune">
                          Herejes de Dune / Heretics of Dune
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-10">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9788466359399" data-imgurl="prodimage.images-bn.com/pimages/9788466359399_p0_v1_s90x140.jpg" data-pdpurl="/w/herejes-de-dune-heretics-of-dune/frank-herbert/1140077613" data-synopsis=" " data-title="Herejes de Dune / Heretics of Dune" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/missing-link/frank-herbert/1017475339" onclick="set_cookie('emi_/w/missing-link/frank-herbert/1017475339_na_image');" title="view details">
    <noscript>
    <img alt="Missing Link" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9789357727709_p0_v1_s90x140.jpg" title="Missing Link"/>
    </noscript>
    <img alt="Missing Link" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9789357727709_p0_v1]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/missing-link/frank-herbert/1017475339" onclick="set_cookie('emi_Missing Link_na_text');" title="Missing Link">
                          Missing Link
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-11">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9789357727709" data-imgurl="prodimage.images-bn.com/pimages/9789357727709_p0_v1_s90x140.jpg" data-pdpurl="/w/missing-link/frank-herbert/1017475339" data-synopsis=" " data-title="Missing Link" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/god-emperor-of-dune/frank-herbert/1002078831" onclick="set_cookie('emi_/w/god-emperor-of-dune/frank-herbert/1002078831_na_image');" title="view details">
    <noscript>
    <img alt="God Emperor of Dune" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780593098257_p0_v1_s90x140.jpg" title="God Emperor of Dune"/>
    </noscript>
    <img alt="God Emperor of Dune" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780593098257_p0_v1]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/god-emperor-of-dune/frank-herbert/1002078831" onclick="set_cookie('emi_God Emperor of Dune_na_text');" title="God Emperor of Dune">
                          God Emperor of Dune
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-12">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780593098257" data-imgurl="prodimage.images-bn.com/pimages/9780593098257_p0_v1_s90x140.jpg" data-pdpurl="/w/god-emperor-of-dune/frank-herbert/1002078831" data-synopsis=" " data-title="God Emperor of Dune" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/the-dragon-in-the-sea/frank-herbert/1101126130" onclick="set_cookie('emi_/w/the-dragon-in-the-sea/frank-herbert/1101126130_na_image');" title="view details">
    <noscript>
    <img alt="The Dragon in the Sea" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780765317742_p0_v3_s90x140.jpg" title="The Dragon in the Sea"/>
    </noscript>
    <img alt="The Dragon in the Sea" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780765317742_p0_v3]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/the-dragon-in-the-sea/frank-herbert/1101126130" onclick="set_cookie('emi_The Dragon in the Sea_na_text');" title="The Dragon in the Sea">
                          The Dragon in the Sea
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-13">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780765317742" data-imgurl="prodimage.images-bn.com/pimages/9780765317742_p0_v3_s90x140.jpg" data-pdpurl="/w/the-dragon-in-the-sea/frank-herbert/1101126130" data-synopsis=" " data-title="The Dragon in the Sea" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/the-collected-stories-of-frank-herbert/frank-herbert/1120085144" onclick="set_cookie('emi_/w/the-collected-stories-of-frank-herbert/frank-herbert/1120085144_na_image');" title="view details">
    <noscript>
    <img alt="The Collected Stories of Frank Herbert" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780765336972_p0_v3_s90x140.jpg" title="The Collected Stories of Frank Herbert"/>
    </noscript>
    <img alt="The Collected Stories of Frank Herbert" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780765336972_p0_v3]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/the-collected-stories-of-frank-herbert/frank-herbert/1120085144" onclick="set_cookie('emi_The Collected Stories of Frank Herbert_na_text');" title="The Collected Stories of Frank Herbert">
                          The Collected Stories of Frank Herbert
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-14">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780765336972" data-imgurl="prodimage.images-bn.com/pimages/9780765336972_p0_v3_s90x140.jpg" data-pdpurl="/w/the-collected-stories-of-frank-herbert/frank-herbert/1120085144" data-synopsis=" " data-title="The Collected Stories of Frank Herbert" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    <div class="product-shelf-tile" role="option">
    <div class="product-shelf-image-cont" data-match-height="product-shelf-image">
    <div class="product-shelf-image">
    <a class="image-container carousel-image-link" href="/w/the-green-brain/frank-herbert/1102124587" onclick="set_cookie('emi_/w/the-green-brain/frank-herbert/1102124587_na_image');" title="view details">
    <noscript>
    <img alt="The Green Brain" class="full-shadow" data-bottom-align="" src="//prodimage.images-bn.com/pimages/9780765378897_p0_v2_s90x140.jpg" title="The Green Brain"/>
    </noscript>
    <img alt="The Green Brain" class="Resolve lp-lazy full-shadow" data-bottom-align="" data-resolvechain="product=path[/pimages/9780765378897_p0_v2]&amp;call=url[file:common/decodeProduct.chain]" src="//img.images-bn.com/static/redesign/srcs/images/grey-box.png?v11.4.4"/>
    </a>
    </div>
    </div>
    <div class="product-shelf-info text-center">
    <div class="product-shelf-title explore-more-title">
    <a href="/w/the-green-brain/frank-herbert/1102124587" onclick="set_cookie('emi_The Green Brain_na_text');" title="The Green Brain">
                          The Green Brain
                         </a>
    </div>
    <div class="explore-more-description" id="exploreMoreDescription-15">
    </div>
    <div class="explore-more-see-details">
    <a class="view-full-ei-details" data-ean="9780765378897" data-imgurl="prodimage.images-bn.com/pimages/9780765378897_p0_v2_s90x140.jpg" data-pdpurl="/w/the-green-brain/frank-herbert/1102124587" data-synopsis=" " data-title="The Green Brain" href="javascript:void(0);">
                          See Details
                         </a>
    </div>
    </div>
    </div>
    </div>
    </section>
    </div>
    </div>
    </div>
    </div>
    </div>
    <script>
                if(typeof performance.mark !== 'undefined')
    {
    performance.mark("Global_Footer_loading_starts");
    }
               </script>
    <div class="d-none" id="footer">
    </div>
    <!-- ATG-26331 remove google analytics-->
    <script>
                if(typeof performance.mark !== 'undefined' && typeof performance.measure !== 'undefined')
    {
    performance.mark("Global_Footer_loading_ends");
    performance.measure(
    "globalFooterDur",
    "Global_Footer_loading_starts",
    "Global_Footer_loading_ends"
    );
    }
               </script>
    <!-- ATG-26338 : Add modal for PDP, PLP -->
    <!-- ATG-26338 : Ends -->
    <!-- ATG-28414: Add modal for ROPIS -->
    <!-- ATG-28414: Ends -->
    <script>
                var isresponsive= true;
               </script>
    <!-- All Javascripts in js-scripts-ra.jsp has to be minified. ALl JS has to be moved to release dir as per grunt minification -->
    <script src="//js.js-bn.com/static/redesign/release/js/bn.js?v11.4.4">
    </script>
    <script async="true" src="//js.js-bn.com/static/redesign/release/js/modal.modals-browsepdp.js?v11.4.4">
    </script>
    <script src="//js.js-bn.com/static/redesign/release/js/modal.modals-checkout.js?v11.4.4">
    </script>
    <script src="//js.js-bn.com/static/redesign/release/js/modal.modals-ropis.js?v11.4.4">
    </script>
    <script>
                $.webshims.setOptions('basePath','//js.js-bn.com/static/redesign/srcs/js/vendor/js-webshim-1.15/minified/shims/');
    $.webshims.polyfill('es5 forms forms-ext');
               </script>
    <script async="true" defer="true" src="//js.js-bn.com/static/redesign/release/js/pdp.js?v11.4.4">
    </script>
    <script async="" src="//js.js-bn.com/static/release/js/toolkit-responsive.js?v11.4.4" type="text/javascript">
    </script>
    <script src="//prodimage.images-bn.com/zap/dhtml/com.liquidpixels.Zoom.jsr" type="text/javascript">
    </script>
    <script async="true" defer="true" src="//js.js-bn.com/static/redesign/release/js/audiobook.main.js?v11.4.4">
    </script>
    <script async="" defer="" src="https://request.eprotect.vantivcnp.com/eProtect/eProtect-api3.js" type="text/javascript">
    </script>
    <script async="true" defer="true" src="//js.js-bn.com/static/redesign/release/js/worldpay.js?v11.4.4">
    </script>
    <script src="//js.js-bn.com/static/redesign/release/js/ropis.js?v11.4.4">
    </script>
    <input id="analyticsEnabledFlag" type="hidden" value="true">
    <script>
                if(!$.isEmptyObject(digitalData)){
    var digitalData1 = {"product":[{"category":{"primaryCategory":"Books","subCategory":["Science Fiction - Ecological","Science Fiction - Science & Religion","Science Fiction - Societies & Cultures","Science Fiction - Strange & Alien Worlds"],"productType":"book"},"price":{"basePrice":25.99},"productInfo":{"departmentCode":"8","sku":"9780593201893","productName":"Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune","productID":"prd9780593201893","productURL":"/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893"},"attributes":{"outOfStock":false,"reviews":0,"isDeviceProduct":false,"isDigitalProduct":false,"pickupInStoreStatus":"instore pickup available:geo or store unselected","isEbookProduct":false,"isPhysicalProduct":true,"rating":0,"isIosAvailable":true,"isNOOKProduct":false,"notifyWhenStocked":false}}],"session":{"sessionID":"59A4A13ADB80E3C95F91B52C84746CC6","serverName":"prodny_store02"},"page":{"timestamp":"Mon Apr 01 21:35:49 EDT 2024","category":{"hierarchy":""},"pageInfo":{"pageType":"pdp","pageName":"pdp:frank-herberts-dune-saga-3-book-boxed-set-dune-dune-messiah-and-children-of-dune|1136810577","language":"en","geoRegion":"US","breadCrumbs":["home"],"ipAddress":"73.115.155.43"}},"cart":{"price":{"shipping":0,"priceWithTax":0,"transationalTotal":0,"basePrice":0,"currency":"USD"}},"user":[{"profile":[{"profileInfo":{"profileID":"69985064008"}}]}]};
    $.extend(digitalData,digitalData1);
    }else{
    
    var digitalData = {"product":[{"category":{"primaryCategory":"Books","subCategory":["Science Fiction - Ecological","Science Fiction - Science & Religion","Science Fiction - Societies & Cultures","Science Fiction - Strange & Alien Worlds"],"productType":"book"},"price":{"basePrice":25.99},"productInfo":{"departmentCode":"8","sku":"9780593201893","productName":"Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune","productID":"prd9780593201893","productURL":"/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893"},"attributes":{"outOfStock":false,"reviews":0,"isDeviceProduct":false,"isDigitalProduct":false,"pickupInStoreStatus":"instore pickup available:geo or store unselected","isEbookProduct":false,"isPhysicalProduct":true,"rating":0,"isIosAvailable":true,"isNOOKProduct":false,"notifyWhenStocked":false}}],"session":{"sessionID":"59A4A13ADB80E3C95F91B52C84746CC6","serverName":"prodny_store02"},"page":{"timestamp":"Mon Apr 01 21:35:49 EDT 2024","category":{"hierarchy":""},"pageInfo":{"pageType":"pdp","pageName":"pdp:frank-herberts-dune-saga-3-book-boxed-set-dune-dune-messiah-and-children-of-dune|1136810577","language":"en","geoRegion":"US","breadCrumbs":["home"],"ipAddress":"73.115.155.43"}},"cart":{"price":{"shipping":0,"priceWithTax":0,"transationalTotal":0,"basePrice":0,"currency":"USD"}},"user":[{"profile":[{"profileInfo":{"profileID":"69985064008"}}]}]};
    
    }
    if (typeof s_setP !== 'undefined') {
    s_setP('digitalData.component[0].componentInfo.componentName','more in this series');
    s_setP('digitalData.component[0].componentInfo.componentLocation','pdp-productmaincontent');
    s_setP('digitalData.component[0].componentInfo.primaryCategory','internal campaign');
    s_setP('digitalData.component[1].componentInfo.componentName','you may also like');
    s_setP('digitalData.component[1].componentInfo.componentLocation','pdp-productmaincontent');
    s_setP('digitalData.component[1].componentInfo.primaryCategory','internal campaign');
    s_setP('digitalData.component[2].componentInfo.componentName','recently-viewed');
    s_setP('digitalData.component[2].componentInfo.componentLocation','pdp-productmaincontent');
    s_setP('digitalData.component[2].componentInfo.primaryCategory','internal campaign');
    
    }
    $(document).ready(function(){
    if (typeof s_setP !== 'undefined') {
    
    BN.Analytics.PDP.init();
    
    }
    });
               </script>
    <script type="text/javascript">
    </script>
    <input name="bopisEnabled" type="hidden" value="true"/>
    <script type="text/javascript">
                 var cname = "internalCampaign",
    cvalue = null;
    var curCookie = cname + "=" + cvalue +
    "; expires= Thu, 01 Jan 1970 00:00:01 GMT;" +
    "; path=" + "/"  +
    "; domain=" + SITE_DOMAIN;
    document.cookie = curCookie;
                </script>
    <input id="bopisEligibleMessage" type="hidden" value="storeNotAvailable"/>
    <input id="productSkuId" type="hidden" value="9780593201893"/>
    <input id="productPId" type="hidden" value="prd9780593201893"/>
    <input id="listPrice" type="hidden" value="30.97"/>
    <input id="salePrice" type="hidden" value="25.99"/>
    <input id="availabilityStatus" type="hidden" value="1000">
    <input id="skuType" type="hidden" value="book">
    <script>
                      var bopisEligibiltyMessage = $('#bopisEligibleMessage').val();
    var storeName = $('#storeName').val();
    var storeID = $('#storeID').val();
    if(typeof s_setP !== 'undefined') {
    if(s_getP('digitalData.user[0].profile[0].profileInfo.storeName') == undefined){
    s_setP('digitalData.user[0].profile[0].profileInfo.storeName', storeName);
    s_setP('digitalData.user[0].profile[0].profileInfo.storeID', storeID);
    }
    if(bopisEligibiltyMessage == 'productAvailable'){
    s_setP('digitalData.product[0].attributes.pickupInStoreStatus', 'instore pickup available:geo or store selected');
    }
    else if((bopisEligibiltyMessage == 'productNotAvailable') || (bopisEligibiltyMessage == 'notEligibleForBopis')){
    s_setP('digitalData.product[0].attributes.pickupInStoreStatus', 'instore pickup unavailable:geo or store selected');
    }
    else if(bopisEligibiltyMessage == 'storeNotAvailable'){
    s_setP('digitalData.product[0].attributes.pickupInStoreStatus', 'instore pickup available: geo or store unselected');
    }
    }
                     </script>
    <script type="text/javascript">
                      /*Check id google ad needs to be loaded after page load*/
    
    var asyncRelatedAdsEnabled = true;
    var endemicAd = true;
    $(document).on('googleRelatedAdsLoaded', function() {
    
    })
                     </script>
    <input id="gptAdsVal" name="gptAdsVal" type="hidden" value="">
    <input id="hiddenCardNumber" type="hidden">
    <input id="hiddenSecurityCode" type="hidden">
    <input id="isWPApiAlreadyCalled" type="hidden" value="false">
    <input id="paymentFormContainerId" type="hidden" value=""/>
    <input id="isWorldPayEnabled" type="hidden" value="true">
    <script type="text/javascript">
                       _satellite.pageBottom();
                      </script>
    <script>
                       document.write("<script type='text/javascript' src='//js.js-bn.com/static/redesign/release/js/commerce-footer.js?v11.4.4'><\/script>");
                      </script>
    <script type="text/javascript">
                       /*CommerceHeaderFooter is the name of the library that we defined in webpack.config.js */
    CommerceHeaderFooter.showFooter('footer', {env:'prod', consumer_host:'https://www.barnesandnoble.com', styling:'responsive'});
                      </script>
    <noscript>
    <img src="https://www.barnesandnoble.com/akam/13/pixel_7cec613e?a=dD1mYTc5NTE4MjgxNmRlOTUyZGViZDc0MDNjNTVkNjM4MGU4NzM2N2MzJmpzPW9mZg==" style="visibility: hidden; position: absolute; left: -999px; top: -999px;"/>
    </noscript>
    <script src="/XTbXdBQNGea17GK00jIH/1J1p6GmcDfbO/JGYDCm02CA/WQohHws/SGmg" type="text/javascript">
    </script>
    </input>
    </input>
    </input>
    </input>
    </input>
    </input>
    </input>
    </input>
    </div>
    </main>
    
    
    </body>
    </html>
    
    


```python
# finding the title of the book
title = soup2.find_all(itemprop="name")[-1].get_text().strip()
print(title)
```

    Frank Herbert's Dune Saga 3-Book Boxed Set: Dune, Dune Messiah, and Children of Dune
    


```python
# two different methods to find the price
# method 1
price1 = float(soup2.find('span', {"id": "pdp-cur-price"}).get_text().strip()[1:])
print(price1)
```

    25.99
    


```python
# method 2
price2 = soup2.find(id="pdp-cur-price").get_text().strip()
print(price2[1:])
```

    25.99
    


```python
# when I automate the csv export, I want the date it was exported to be included in the report
today = datetime.date.today()
```


```python
header = ['Book Title', 'Price', 'Date']
data = [title, price1, today]

with open('DuneWebScraper.csv', 'w', newline='', encoding='UTF8') as f:
    writer = csv.writer(f)
    writer.writerow(header)
    writer.writerow(data)
```


```python
import pandas as pd

df = pd.read_csv(r"C:\Users\micha\Projects\my_projects\DuneWebScraper.csv")

print(df)
```

                                              Book Title  Price        Date
    0  Frank Herbert's Dune Saga 3-Book Boxed Set: Du...  25.99  2024-04-01
    


```python
# append the data

with open('DuneWebScraper.csv', 'a+', newline='', encoding='UTF8') as f:
    writer = csv.writer(f)
    writer.writerow(data)
```


```python
# sending an email to myself when the book is selling for less than $15

def send_mail():
    server = smtplib.SMTP_SSL('smtp.gmail.com',465)
    server.ehlo()
    server.ehlo()
    server.login('<my email','<my password>')
    
    subject = "Dune 3 Book Set is now less than $15!"
    body = "Get the Dune 3-Book Set you've been waiting for here: https://www.barnesandnoble.com/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893"
    
    msg = f"Subject: {subject}\n\n{body}"
    
    server.sendmail(
        '<my email>',
        msg
     
    )
```


```python
# function to run for automating

def check_price():
    URL = 'https://www.barnesandnoble.com/w/frank-herberts-dune-saga-3-book-boxed-set-frank-herbert/1136810577?ean=9780593201893'

    headers = {"from my computer"}

    page = requests.get(URL, headers=headers) # connecting our computer to the URL

    soup1 = BeautifulSoup(page.content, "html.parser")

    soup2 = BeautifulSoup(soup1.prettify(), "html.parser")

    title = soup2.find_all(itemprop="name")[-1].get_text().strip()

    price1 = float(soup2.find('span', {"id": "pdp-cur-price"}).get_text().strip()[1:])
    
    import datetime
    
    today = datetime.date.today()
    
    import csv

    header = ['Book Title', 'Price', 'Date']
    data = [title, price1, today]

    with open('DuneWebScraper.csv', 'a+', newline='', encoding='UTF8') as f:
        writer = csv.writer(f)
        writer.writerow(data)

    # send an email if the price falls below $15
    
    if(price1 < 15):
        send_mail()

```


```python
while(True):
    check_price()
    time.sleep(604800) # runs every week (every 604,800 seconds)
```
