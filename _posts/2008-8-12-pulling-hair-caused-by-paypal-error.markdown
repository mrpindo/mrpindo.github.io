---
layout: post
title:  "Pulling hair caused by paypal error"
date:   2008-8-12 14:38:36 +0700
categories: error stack
---



Original sample:
`{'update_time': '2008-02-06T09:15:27Z', 'transactions': [{'description': 'This is the payment transaction description.', 'item_list': {'items': [{'quantity': '1', 'currency': 'USD', 'price': '5.00', 'sku': '78YY', 'name': 'Ayam Goreng Tepung'}, {'quantity': '1', 'currency': 'USD', 'price': '2.80', 'sku': '345D', 'name': 'Barang baru'}]}, 'amount': {'details': {'subtotal': '7.80'}, 'total': '7.80', 'currency': 'USD'}, 'related_resources': [{'sale': {'create_time': '2008-02-06T09:15:17Z', 'state': 'completed', 'parent_payment': 'PAY-6P657247UA5329244KLZVFJI', 'update_time': '2008-02-06T09:15:27Z', 'id': '3SB09053GW117121W', 'links': [{'href': 'https://api.sandbox.paypal.com/v1/payments/sale/3SB09053GW117121W', 'method': 'GET', 'rel': 'self'}, {'href': 'https://api.sandbox.paypal.com/v1/payments/sale/3SB09053GW117121W/refund', 'method': 'POST', 'rel': 'refund'}, {'href': 'https://api.sandbox.paypal.com/v1/payments/payment/PAY-6P657247UA5329244KLZVFJI', 'method': 'GET', 'rel': 'parent_payment'}], 'amount': {'total': '7.80', 'currency': 'USD'}}}]}], 'create_time': '2008-02-06T09:15:17Z', 'intent': 'sale', 'id': 'PAY-6P657247UA5329244KLZVFJI', 'payer': {'funding_instruments': [{'credit_card': {'first_name': 'Asep', 'last_name': 'Basu', 'type': 'visa', 'expire_month': '7', 'number': 'xxxxxxxxxxxx0331', 'expire_year': '2008'}}], 'payment_method': 'credit_card'}, 'links': [{'href': 'https://api.sandbox.paypal.com/v1/payments/payment/PAY-6P657247UA5329244KLZVFJI', 'method': 'GET', 'rel': 'self'}], 'state': 'approved'}`


`Payment ERROR: {'details': [{'field': 'payer.payment_method', 'issue': 'Value is invalid (must be credit_card or paypal)'}, {'field': 'payer', 'issue': 'For credit_card payment method, the supported funding instrument is credit_card or cardit_card_token '}], 'debug_id': '7acdff59c721e', 'name': 'VALIDATION_ERROR', 'information_link': 'https://developer.paypal.com/webapps/developer/docs/api/#VALIDATION_ERROR', 'message': 'Invalid request - see details'}`
