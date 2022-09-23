# Custom Form Contact

<!-- DOCS-IGNORE:start -->
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->


<!-- ALL-CONTRIBUTORS-BADGE:END -->
<!-- DOCS-IGNORE:end -->


The contact form is an app design to create dynamics forms through the information received it by props, for each type like input, select, text area and ReCAPTCHA, the app was developed with Reactjs and Grahql. All the information of each input is sent it to master data.

## Configuration

 - Add the app as a dependency in your store theme

```
"vendorName.contact-form": "0.x"
```

 - Example how integrate the app. 
    The value of the dataEntity depends the name on masterdata, for this example the value is CF

![Custom Form Contact](https://i.ibb.co/gmYM4T2/dataentities.png)

```
{
    "store.custom#contacto":{
        "blocks": ["formulario#dinamico"]
    },
   ...
   "formulario#dinamico":{
      "props":{
        "dataEntity": "CF"
      },
        "children": [
          "flex-layout.row#name",
          "flex-layout.row#email",
          "flex-layout.row#rut",
          "flex-layout.row#phone",
          "flex-layout.row#order",
          "flex-layout.row#reason",
          "flex-layout.row#message",
          "flex-layout.row#captcha",
          "flex-layout.row#submit"
        ]
      },
}
```

```
{
   "input#name":{
        "props":{
            "nameInput": "name",
            "placeholder": "type a name",
            "id": "nameid", 
            "type": "text",
            "typeValidation": "letters",
            "label": "name"
        }
      },
    ...

    ...
      "input#submit":{
        "props":{
         "type": "submit"
        }
      }
}
```

 - Configuration of queries.
    -The value of account has to be the same as vendor on the store manifest.json, as shown in the picture below.

![Custom Form Contact](https://i.ibb.co/9TpQM0S/Queries.png)

## Type of inputs, validation and properties.

The dynamic form has 4 type of component and each one has different validation and properties. For all case, the props nameInput is required.

### Input
 - This is an example how declare a input component:
    ```
        "input#name":{
            "props":{
            "nameInput": "name",
            "placeholder": "type a name",
            " id": "nameid", 
            "type": "text",
            "typeValidation": "letters",
            "label": " name "
            }
        },
    ```   

### Properties of Input.

  - **nameInput:**   string *Name of the input, this is the key and must be the same name on master Data*

  - **placeholder:**  string *Text to show as placeholder*

  -  **id:** string  *Input ID*

  - **label:**  string *Input label*

  - **type:** string *Type of the input, for more information we recomend check the next [url]*

  - **required:** Boolean *Default value is false, if the input is required change to true*

  - **minlength:** Integer *minimum input length*

  - **maxlength:** Integer *maximum input length*

  - **readonly:**  Boolean *True if the input is readonly*
  
  - **value:** String *Value of the input*
  
  - **typeValidation:**  String *The typeValidation is a special validation made on JS, email, number, letters, curp,rut. Each one validate one type, like if input is a validate email or not*
       
  - **errorText** String *Text to show on error, this working only with the TypeValidation*

[url]: https://www.w3schools.com/html/html_form_input_types.asp

### Select
 - This is an example how declare a select component:

   ```
        "select#reason":{
            "props":{
            "name": "Reason",
            "id": "reason", 
            "label": "Reason",
            "valueObj": [
            {
                "value": "value on selection 0",
                "text": "value on selection 0"
            },
            {
                "value": "value on selection 1",
                "text": "Text on selection 1",
                "selected": true,
            },
            {
                "value": "value on selection 2",
                "text": "Text on selection 2"
            },
            {
                "value": "value on selection 3",
                "text": "Text on selection 3"
            },

            {
                "value": "value on selection 4",
                "text": "Text on selection 4"
            }
            ]
            }
        }, 
    ```

### Properties of Select.

  - **name:**  string *Name of the input, this is the key and must be the same name on master Data*

  - **id:** string  *Input ID*

  - **label:**  string *Input label*

  - **selectMessage:**  string *Message from selected input*

  - **valueObj:** object *Receive a object value and the properties are: value, text and selected this last one is a optional value as true, the default value of selected is false*
 
### TextArea.

 - This is an example how declare a TextArea component:

    ```
    "textarea#mensaje":{
            "props":{
            "nameInput": "message",
            "placeholder": "type a message",
            "id": "message", 
            "label": "message",
            "rows": "4",
            "cols": "50"
            }
        },
    ```

### Properties of TextArea.

 - **nameInput:**  string *Name of the input, this is the key and must be the same name on master Data*

 - **id:** string  *Input ID*

 - **label:**  string *Input label*

 - **minlength:** Integer *minimum input length*

 - **maxlength:** Integer *maximum input length*

 - **required:** Boolean *Default value is false, if the input is required change to true*

 - **readonly:**  Boolean *True if the input is readonly*

 - **rows:** Integer *The number of visible lines*
 
 - **cols:** Integer *The visible width of the text control, in half-width characters. If it is defined, it must be positive. If not, the default value is 20*

### Captcha.

 - This is an example how declare a Captcha component:
    
    ```
   "captcha#ecomsur":{
        "props":{
          "captchaKey": "keyGenerateByGoogle"
        }
      },
     ```  

### Properties of Captcha.

 - **captchaKey:**  string *This is a key generated by Google, you need to created it in the Google Panel Administrator and add the URL from the project. This props is required. The google version of the captcha is V2. For more information you can read on [Google]*

[Google]: https://developers.google.com/recaptcha/docs/display

## MasterData and the dynamycs inputs.

The name of the input has to be the same name on masterdata. How you can see in the example below with email and name.

### Name in Master Data

![Custom Form Contact](https://i.ibb.co/FHGGq4t/master-Data.png)


### Name in Dynamic Form

![Custom Form Contact](https://i.ibb.co/TLwSx4X/masterdata-Name.png)

<!-- DOCS-IGNORE:start -->

## Contributors ✨

Thanks goes to these wonderful people:

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
- Carlos Deseda
- Duglas Medina
- Jose Martinez

<!-- DOCS-IGNORE:end -->
