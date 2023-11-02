---
layout: default-layout
title: interface IntermediateResultReceiver - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface IntermediateResultReceiver in Dynamsoft Core Module.
keywords: intermediate result receiver, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultReceiver

The `IntermediateResultReceiver` interface is responsible for receiving intermediate results of different types. It provides virtual functions for each type of result, which are called when the corresponding result is received.

## Definition

```typescript
interface IntermediateResultReceiver {
  getObservationParameters(): ObservationParameters;
  onTaskResultsReceived?(result: IntermediateResult, info: IntermediateResultExtraInfo): void;
  onPredetectedRegionsReceived?(result: PredetectedRegionsUnit, info: IntermediateResultExtraInfo): void;
  onLocalizedBarcodesReceived?(result: DBR.IntermediateResult.LocalizedBarcodesUnit, info: IntermediateResultExtraInfo): void;
  onDecodedBarcodesReceived?(result: DBR.IntermediateResult.DecodedBarcodesUnit, info: IntermediateResultExtraInfo): void;
  onLocalizedTextLinesReceived?(result: DLR.IntermediateResult.LocalizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
  onRecognizedTextLinesReceived?(result: DLR.IntermediateResult.RecognizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
  onDetectedQuadsReceived?(result: DDN.IntermediateResult.DetectedQuadsUnit, info: IntermediateResultExtraInfo): void;
  onNormalizedImagesReceived?(result: DDN.IntermediateResult.NormalizedImagesUnit, info: IntermediateResultExtraInfo): void;
  onColourImageUnitReceived?(result: ColourImageUnit, info: IntermediateResultExtraInfo): void;
  onScaledDownColourImageUnitReceived?(result: ScaledDownColourImageUnit, info: IntermediateResultExtraInfo): void;
  onGrayscaleImageUnitReceived?(result: GrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
  onTransformedGrayscaleImageUnitReceived?(result: TransformedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
  onEnhancedGrayscaleImageUnitReceived?(result: EnhancedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
  onBinaryImageUnitReceived?(result: BinaryImageUnit, info: IntermediateResultExtraInfo): void;
  onTextureDetectionResultUnitReceived?(result: TextureDetectionResultUnit, info: IntermediateResultExtraInfo): void;
  onTextureRemovedGrayscaleImageUnitReceived?(result: TextureRemovedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
  onTextureRemovedBinaryImageUnitReceived?(result: TextureRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
  onContoursUnitReceived?(result: ContoursUnit, info: IntermediateResultExtraInfo): void;
  onLineSegmentsUnitReceived?(result: LineSegmentsUnit, info: IntermediateResultExtraInfo): void;
  onTextZonesUnitReceived?(result: TextZonesUnit, info: IntermediateResultExtraInfo): void;
  onTextRemovedBinaryImageUnitReceived?(result: TextRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
  onLongLinesUnitReceived?(result: DDN.IntermediateResult.LongLinesUnit, info: IntermediateResultExtraInfo): void;
  onCornersUnitReceived?(result: DDN.IntermediateResult.CornersUnit, info: IntermediateResultExtraInfo): void;
  onCandidateQuadEdgesUnitReceived?(result: DDN.IntermediateResult.CandidateQuadEdgesUnit, info: IntermediateResultExtraInfo): void;
  onCandidateBarcodeZonesUnitReceived?(result: DBR.IntermediateResult.LocalizedBarcodesUnit, info: IntermediateResultExtraInfo): void;
  onScaledUpBarcodeImageUnitReceived?(result: DBR.IntermediateResult.ScaledUpBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
  onDeformationResistedBarcodeImageUnitReceived?(result: DBR.IntermediateResult.DeformationResistedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
  onComplementedBarcodeImageUnitReceived?(result: DBR.IntermediateResult.ComplementedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
}

```


| API Name | Description |
|--------|-------------|
| [`getObservedParameters()`](#getobservedparameters) | Gets the types of intermediate result units that have been observed. |
| [`onTaskResultsReceived()`](#ontaskresultsreceived) | Called when a task result has been received. |
| [`onPredetectedRegionsReceived()`](#onpredetectedregionsreceived) | Called when predetected regions have been received. |
| [`onLocalizedBarcodesReceived()`](#onlocalizedbarcodesreceived) | Called when localized barcodes have been received. |
| [`onDecodedBarcodesReceived()`](#ondecodedbarcodesreceived) | Called when decoded barcodes have been received. |
| [`onLocalizedTextLinesReceived()`](#onlocalizedtextlinesreceived) | Called when localized text lines have been received. |
| [`onRecognizedTextLinesReceived()`](#onrecognizedtextlinesreceived) | Called when recognized text lines have been received. |
| [`onDetectedQuadsReceived()`](#ondetectedquadsreceived) | Called when detected quadrilaterals have been received. |
| [`onNormalizedImagesReceived()`](#onnormalizedimagesreceived) | Called when normalized images have been received. |
| [`onColourImageUnitReceived()`](#oncolourimageunitreceived) | Called when colour image units have been received. |
| [`onScaledDownColourImageUnitReceived()`](#onscaleddowncolourimageunitreceived) | Called when scaled down colour image units have been received. |
| [`onGrayscaleImageUnitReceived()`](#ongrayscaleimageunitreceived) | Called when grayscale image units have been received. |
| [`onTransformedGrayscaleImageUnitReceived()`](#ontransformedgrayscaleimageunitreceived) | Called when transformed grayscale image units have been received. |
| [`onEnhancedGrayscaleImageUnitReceived()`](#onenhancedgrayscaleimageunitreceived) | Called when enhanced grayscale image units have been received. |
| [`onBinaryImageUnitReceived()`](#onbinaryimageunitreceived) | Called when binary image units have been received. |
| [`onTextureDetectionResultUnitReceived()`](#ontexturedetectionresultunitreceived) | Called when texture detection result units have been received. |
| [`onTextureRemovedGrayscaleImageUnitReceived()`](#ontextureremovedgrayscaleimageunitreceived) | Called when texture removed grayscale image units have been received. |
| [`onTextureRemovedBinaryImageUnitReceived()`](#ontextureremovedbinaryimageunitreceived) | Called when texture removed binary image units have been received. |
| [`onContoursUnitReceived()`](#oncontoursunitreceived) | Called when contour units have been received. |
| [`onLineSegmentsUnitReceived()`](#onlinesegmentsunitreceived) | Called when line segment units have been received. |
| [`onTextZonesUnitReceived()`](#ontextzonesunitreceived) | Called when text zone units have been received. |
| [`onTextRemovedBinaryImageUnitReceived()`](#ontextremovedbinaryimageunitreceived) | Called when text removed binary image units have been received. |
| [`onLongLinesUnitReceived()`](#onlonglinesunitreceived) | Called when long line units have been received. |
| [`onCornersUnitReceived()`](#oncornersunitreceived) | Called when corner units have been received. |
| [`onCandidateQuadEdgesUnitReceived()`](#oncandidatequadedgesunitreceived) | Called when candidate quadrilateral edge units have been received. |
| [`onCandidateBarcodeZonesUnitReceived()`](#oncandidatebarcodezonesunitreceived) | Called when candidate barcode zone units have been received. |
| [`onScaledUpBarcodeImageUnitReceived()`](#onscaledupbarcodeimageunitreceived) | Called when scaled up barcode image units have been received. |
| [`onDeformationResistedBarcodeImageUnitReceived()`](#ondeformationresistedbarcodeimageunitreceived) | Called when deformation resisted barcode image units have been received. |
| [`onComplementedBarcodeImageUnitReceived()`](#oncomplementedbarcodeimageunitreceived) | Called when complemented barcode image units have been received. |

### getObservedParameters

Gets the observed parameters of the intermediate result receiver.

```typescript
getObservationParameters(): ObservationParameters;
```

**Return value**

Returns the object of CObservedParameters. The default parameters are to observe all intermediate result unit types and all tasks.

### onTaskResultsReceived

Called when a task result has been received.

```typescript
onTaskResultsReceived?(result: IntermediateResult, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The IntermediateResult object that contains several result units.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onPredetectedRegionsReceived

Called when predetected regions have been received.

```typescript
onPredetectedRegionsReceived?(result: PredetectedRegionsUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The PredetectedRegionsUnit object that contains the result.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onLocalizedBarcodesReceived

Called when localized barcodes have been received.

```typescript
onLocalizedBarcodesReceived?(result: DBR.IntermediateResult.LocalizedBarcodesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The LocalizedBarcodesUnit object that contains the result.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onDecodedBarcodesReceived

Called when decoded barcodes have been received.

```typescript
onDecodedBarcodesReceived?(result: DBR.IntermediateResult.DecodedBarcodesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The DecodedBarcodesUnit object that contains the result.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onLocalizedTextLinesReceived

Called when localized text lines have been received.

```typescript
onLocalizedTextLinesReceived?(result: DLR.IntermediateResult.LocalizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The LocalizedTextLinesUnit object that contains the result.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onRecognizedTextLinesReceived

Called when recognized text lines have been received.

```typescript
onRecognizedTextLinesReceived?(result: DLR.IntermediateResult.RecognizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The RecognizedTextLinesUnit object that contains the result.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onDetectedQuadsReceived

Called when detected quadrilaterals have been received.

```typescript
onDetectedQuadsReceived?(result: DDN.IntermediateResult.DetectedQuadsUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The DetectedQuadsUnit object that contains the result.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onNormalizedImagesReceived

Called when normalized images have been received.

```typescript
onNormalizedImagesReceived?(result: DDN.IntermediateResult.NormalizedImagesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The NormalizedImageUnit object that contains the result.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onColourImageUnitReceived

Called when colour image units have been received.

```typescript
onColourImageUnitReceived?(result: ColourImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received colour image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onScaledDownColourImageUnitReceived

Handles the receipt of a scaled-down colour image unit.

```typescript
onScaledDownColourImageUnitReceived?(result: ScaledDownColourImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received scaled-down colour image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onGrayscaleImageUnitReceived

Handles the receipt of a grayscale image unit.

```typescript
onGrayscaleImageUnitReceived?(result: GrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received grayscale image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onTransformedGrayscaleImageUnitReceived

Handles the receipt of a transformed grayscale image unit.

```typescript
onTransformedGrayscaleImageUnitReceived?(result: TransformedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received transformed grayscale image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onEnhancedGrayscaleImageUnitReceived

Handles the receipt of an enhanced grayscale image unit.

```typescript
onEnhancedGrayscaleImageUnitReceived?(result: EnhancedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received enhanced grayscale image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onBinaryImageUnitReceived

Handles the receipt of a binary image unit.

```typescript
onBinaryImageUnitReceived?(result: BinaryImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received binary image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onTextureDetectionResultUnitReceived

Handles the receipt of a texture detection result unit.

```typescript
onTextureDetectionResultUnitReceived?(result: TextureDetectionResultUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received texture detection result unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onTextureRemovedGrayscaleImageUnitReceived

Handles the receipt of a texture-removed grayscale image unit.

```typescript
onTextureRemovedGrayscaleImageUnitReceived?(result: TextureRemovedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received texture-removed grayscale image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onTextureRemovedBinaryImageUnitReceived

Handles the receipt of a texture-removed binary image unit.

```typescript
onTextureRemovedBinaryImageUnitReceived?(result: TextureRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The received texture-removed binary image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onContoursUnitReceived

Handles the receipt of a contours unit.

```typescript
onContoursUnitReceived?(result: ContoursUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The contours unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onLineSegmentsUnitReceived

Called when a line segments unit is received.

```typescript
onLineSegmentsUnitReceived?(result: LineSegmentsUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The line segments unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onTextZonesUnitReceived

Called when a text zones unit is received.

```typescript
onTextZonesUnitReceived?(result: TextZonesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The text zones unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onTextRemovedBinaryImageUnitReceived

Called when a text removed binary image unit is received.

```typescript
onTextRemovedBinaryImageUnitReceived?(result: TextRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The text removed binary image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onLongLinesUnitReceived

Called when a long lines unit is received.

```typescript
onLongLinesUnitReceived?(result: DDN.IntermediateResult.LongLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The long lines unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onCornersUnitReceived

Called when a corners unit is received.

```typescript
onCornersUnitReceived?(result: DDN.IntermediateResult.CornersUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The corners unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onCandidateQuadEdgesUnitReceived

Called when a candidate quad edges unit is received.

```typescript
onCandidateQuadEdgesUnitReceived?(result: DDN.IntermediateResult.CandidateQuadEdgesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The candidate quad edges unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onCandidateBarcodeZonesUnitReceived

Called when a candidate barcode zones unit is received.

```typescript
onCandidateBarcodeZonesUnitReceived?(result: DBR.IntermediateResult.LocalizedBarcodesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The candidate barcode zones unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onScaledUpBarcodeImageUnitReceived

Called when a scaled up barcode image unit is received.

```typescript
onScaledUpBarcodeImageUnitReceived?(result: DBR.IntermediateResult.ScaledUpBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The scaled up barcode image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onDeformationResistedBarcodeImageUnitReceived

Called when a deformation resisted barcode image unit is received.

```typescript
onDeformationResistedBarcodeImageUnitReceived?(result: DBR.IntermediateResult.DeformationResistedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The deformation resisted barcode image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.

### onComplementedBarcodeImageUnitReceived

Called when a complemented barcode image unit is received.

```typescript
onComplementedBarcodeImageUnitReceived?(result: DBR.IntermediateResult.ComplementedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The complemented barcode image unit.

`info`: The IntermediateResultExtraInfo object that contains the extra info of intermediate result.
