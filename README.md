# SAP UI5 Demo Basic UI Typo Error Debugging Using SAPUI5 Diagnostics Tools

SAPUI5 Diagnostics Tools are essential for debugging and optimizing the performance of SAPUI5 applications. These tools offer insights into various aspects of your application's runtime behavior, allowing you to identify and resolve issues efficiently.

### Error Explaination:

We have done a small typo in our file  [/webapp/view/InvoicesList.view.xml](https://github.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/blob/master/webapp/view/InvoicesList.view.xml "InvoicesList.view.xml")
which is capital 'T' instead of small t in number attribute binding Ex`T`endedPrice.

#### Result of error
Because of this typo we are unable to see the numbers / currency in our invoices list.

#### Wrong code
```
number = "{
    parts: [
        'invoice>ExTendedPrice',
        'myView>/currency'
    ],
    type: 'sap.ui.model.type.Currency',
    formatOptions: {
        showMeasure: false
    }
}"
```
#### Right code after debug should be:

```
number = "{
    parts: [
        'invoice>ExtendedPrice',
        'myView>/currency'
    ],
    type: 'sap.ui.model.type.Currency',
    formatOptions: {
        showMeasure: false
    }
}"
```


### How to debug this code

Step 1: After running the code press `Ctrl` + `Shift` + `ALT` + `S` (For WINDOWS) or  `control` + `shift` + `option` + `S` (For MAC) 

Step 2: SAPUI5 Diagnostics Tools Will be opened. Click and expand the Control Tree.

Step 3: Click and expand list control and click on 'ObjectListItem0' which is first item in our list.

Step 4: Go to the Binding Infos tab on the right, and scroll down, we can actually see that the binding path of the number attribute is marked as invalid.

Step 5: We found issue now check the spelling and correct it and try re-running the app.

All the steps are shown below with screenshots and also a video link for same is here: [How To Debug](https://github.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/raw/master/How%20to%20debug%20-%20Video/HowToDebug.mp4 "How To Debug")

---

[![Vaibhav Mojidra - 1.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/master/screenshot/1.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - 2.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/master/screenshot/2.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - 3.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/master/screenshot/3.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - 4.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/master/screenshot/4.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - 5.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/master/screenshot/5.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - HowToDebugUI.gif](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Basic-UI-Typo-Error-Debugging-Using-SAPUI5-Diagnostics-Tools/master/screenshot/HowToDebugUI.gif "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)
