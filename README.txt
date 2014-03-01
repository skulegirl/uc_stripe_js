uc_stripe_js
============

drupal module to support stripe.js checkout

I borrowed a lot of this from the existing uc_stripe module, but I wanted to use the Stripe Checkout option.
This doesn't require the uc_credit module, and pops up the pretty little javascript box from the checkout
review page. Advantage of Stripe Checkout is that it is updated by Stripe as needed, and has good mobile support.

There are a couple of hacks specific to my needs in here that should be removed if anyone else wants to use it:
  * The credit cared options are hardcoded to Visa, MC and Amex
  * The product descriptions sent to checkout are hardcoded to values that correspond to my products - I did this
    because the product titles from ubercart were too long, and I was too lazy to make this programmable.
    
The PHP stripe library (https://github.com/stripe/stripe-php) needs to be downloaded and installed into 
sites/all/libraries/stripe such that the path to stripe.php is in sites/all/libraries/stripe/lib/Stripe.php. 

There is no support for recurring payments in here.
