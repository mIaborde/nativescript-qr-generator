# nativescript-qr-generator

NativeScript-Qr-Generator is a plugin for NativeScript which generates Qr code images.

It wraps the following native Qr generators libraries:

**Android:** [https://github.com/kenglxn/QRGen](https://github.com/kenglxn/QRGen)<br />
**iOS:** [https://github.com/gscarrone/iOS-QR-Code-Generator](https://github.com/gscarrone/iOS-QR-Code-Generator)

## Installation

Go to your app's root folder and execute:

```javascript
tns plugin add nativescript-qr-generator
```

## Usage 
	
	```typescript
    import { Component } from "@angular/core";
    import { ImageSource } from "tns-core-modules/image-source";
    import { Image } from "tns-core-modules/ui/image";
    import { QrGenerator } from "nativescript-qr-generator";

    @Component({
        selector: "ns-main",
        template: "<Image src="" (loaded)="onImageLoaded($event)"></Image>"
    })
    export class AppComponent {

        constructor() {} 
        
        onImageLoaded(){
            const image = args.object as Image;
            const result = new QrGenerator().generate('Hello World');
            image.imageSource = new ImageSource(result);
        }
    }
    ```)

## API
    
| Property | Default | Description |
| --- | --- | --- |
| value | - | Value to generate Qr code |
| size.width | 200 | The image's width |
| size.height | 200 | The image's height |
| color | '#000000' | The Qr's color |
| backgroundColor | '#FFFFFFF' | The background's color |
