## survey happy path
* greet
    - utter_greet
* affirm
    - health_form
    - form{"name": "health_form"}
    - form{"name": null}
    - utter_slots_values
* thankyou
    - utter_no_worries
    - utter_goodbye


## person denies to take the survey
* greet
    - utter_greet
* deny
    - utter_goodbye


## survey stop
* greet
    - utter_greet
* affirm
    - health_form
    - form{"name": "health_form"}
* out_of_scope
    - utter_ask_continue
* deny
    - action_deactivate_form
    - form{"name": null}
    - utter_goodbye

## survey continue
* greet
    - utter_greet
* affirm
    - health_form
    - form{"name": "health_form"}
* out_of_scope
    - utter_ask_continue
* affirm
    - health_form
    - form{"name": null}
    - utter_slots_values
