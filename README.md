 Paytabs
Backend side
  1.for make payment : https://secure.paytabs.sa/payment/request
  
  reqest parameter : {
    "profile_id": 87974 /* take it from db (enter from admin panel)*/,
    "tran_type": "sale",
    "tran_class": "ecom",
    "cart_description": "Testing Description of the items/services",
    "cart_id": "Unique order reference" /* create cart id for user */,
    "cart_currency": "SAR",
    "cart_amount": 10,
    "callback": "https://yourdomain.com/yourcallback",
    "return": "https://yourdomain.com/yourpage"
}
  2. for refund : https://secure.paytabs.sa/payment/request
  request paramters : {
    "profile_id": 87974 /* take it from db (enter from admin panel)*/,
    "tran_type": "refund",
    "tran_class" : "ecom",
    "tran_ref": "TST2208100466418" /* take it from db */,
    "cart_id": "9558171717" /* take it from db */,
    "cart_description": "Cart Description",
    "cart_currency": "SAR",
    "cart_amount": 10
  }
API needed for this payment gateway:
createpayment api(parameter : amount) (POST)
refund payment api (parameter : amount) (POST)
send tranzaction reference id api (parameter : id) (POST)
