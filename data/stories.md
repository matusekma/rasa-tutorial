## thank
* thank
  - utter_noworries

## goodbye
* bye
  - utter_bye
  
 ## Some question from FAQ
* faq
  - respond_faq
  
## sales form
* contact_sales
  - utter_sales_ok
  - sales_form                   <!--Run the sales_form action-->
  - form{"name": "sales_form"}   <!--Activate the form-->
  - form{"name": null}           <!--Deactivate the form-->
  
## sales + faq and continue
* contact_sales
    - sales_form
    - form{"name": "sales_form"}
* faq
    - respond_faq
    - utter_still_sales
* yes
    - sales_form
    - form{"name": null}
    
## sales + faq and abort
* contact_sales
    - sales_form
    - form{"name": "sales_form"}
* faq
    - respond_faq
    - utter_still_sales
* no
    - form{"name": null}
    - utter_bye