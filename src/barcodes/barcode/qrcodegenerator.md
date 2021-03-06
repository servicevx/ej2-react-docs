﻿---
title: "QR Code generator"
component: "BarcodeGenerator"
description: "BarcodeGenerator component is a pure JavaScript library which will convert a string to Barcode and show it to the user. This supports major 1D and 2D barcodes including coda bar, code 128, QR Code."
---

# QR Code generator

# QR Code

A QR Code is a two-dimensional barcode that consists of a grid of dark and light dots or blocks that form a square. The data encoded in the barcode can be numeric, alphanumeric, or Shift Japanese Industrial Standards (JIS8) characters. The QR Code uses version from 1 to 40. Version 1 measures 21 modules x 21 modules, Version 2 measures 25 modules x 25 modules, and so on. The number of modules increases in steps of 4 modules per side up to Version 40 that measures 177 modules x 177 modules. Each version has its own capacity. By default, the barcode control automatically set the version according to the length of the input text. The QR Barcodes are designed for industrial uses and also commonly used in consumer advertising.

{% tab template="barcode/qrcode/qrcode", compileJsx=true,  isDefaultActive=true%}

```tsx
import * as React from "react";
import * as ReactDOM from "react-dom";
 import { QRCodeGeneratorComponent  } from '@syncfusion/ej2-react-barcode-generator';


ReactDOM.render(
 <QRCodeGeneratorComponent
    id="barcode"
    width={"200px"}
     height={"150px"}
     value='Syncfusion'
    ></QRCodeGeneratorComponent>,
  document.getElementById("barcode")
);
```

{% endtab %}

## Customizing the Barcode color

A page or printed media with barcode often appears colorful in the background and surrounding region with other contents. In such cases the barcode can also be customized to suit the needs. You can achieve this by using for forecolor property .

{% tab template="barcode/qrcode/qrcode", compileJsx=true,  isDefaultActive=true%}

```tsx
import * as React from "react";
import * as ReactDOM from "react-dom";
 import { QRCodeGeneratorComponent  } from '@syncfusion/ej2-react-barcode-generator';


ReactDOM.render(
 <QRCodeGeneratorComponent
    id="barcode"
    width={"200px"}
     height={"150px"}
     foreColor={"red"}
     value='Syncfusion'
    ></QRCodeGeneratorComponent>,
  document.getElementById("barcode")
);
```

{% endtab %}

## Customizing the Barcode dimension

The dimension of the barcode can be changed using the height and width properties of the barcodegenerator.

{% tab template="barcode/qrcode/dimension", compileJsx=true,  isDefaultActive=true%}

```tsx
import * as React from "react";
import * as ReactDOM from "react-dom";
 import { QRCodeGeneratorComponent  } from '@syncfusion/ej2-react-barcode-generator';


ReactDOM.render(
 <QRCodeGeneratorComponent
    id="barcode"
     width={"100px"}
    height={"100px"}
     value='Syncfusion'
    ></QRCodeGeneratorComponent>,
  document.getElementById("barcode")
);
```

{% endtab %}

## Customizing the text

In barcode generators You can customize the barcode text by using display text property .
{% tab template="barcode/qrcode/text", compileJsx=true,  isDefaultActive=true%}

```tsx
import * as React from "react";
import * as ReactDOM from "react-dom";
 import { QRCodeGeneratorComponent  } from '@syncfusion/ej2-react-barcode-generator';


ReactDOM.render(
 <QRCodeGeneratorComponent
    id="barcode"
     width={"200px"}
     height={"150px"}
    displayText={{ text: "text" }}
     value='Syncfusion'
    ></QRCodeGeneratorComponent>,
  document.getElementById("barcode")
);
```

{% endtab %}