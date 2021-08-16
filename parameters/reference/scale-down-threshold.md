---
title: Dynamsoft Content Normalizer Parameter Reference - ScaleDownThreshold
keywords: scaledownthreshold, parameters, reference, dcn, documentation
description: Dynamsoft Content Normalizer Parameter Reference - ScaleDownThreshold
needGenerateH3Content: true
---


# ScaleDownThreshold
Sets the threshold for the image shrinking.

**Remarks**   
If the shorter edge size is larger than the given value, the library will calculate the required height and width and shrink the image to that size before normalization. Otherwise, it will perform content normalization on the original image.

## Setting Methods
### As Json Parameter

| Parent Json Object | Json Parameter Name | Value Type | 
| ------------------ | ------------------- | ---------- |
| ContentNormalizerParameter | ScaleDownThreshold | *int* |

**Value Range**  
    [512, 0x7fffffff]

**Default Value**  
    2048

**Example**  
```json
{
    "ScaleDownThreshold": 4096,
}
```

### As Struct Member

| Struct | Struct Member Name | Value Type | 
| ------ | ------------------ | ---------- |
| DCN_RuntimeSettings | scaleDownThreshold | *int* |

**Value Range**  
    [512, 0x7fffffff]

**Default Value**  
    2048

**Code Snippet**  
```cpp
// This is a c++ sample code.
ContentNormalizer::InitLicense("t0260NwAAAHV***************");
ContentNormalizer* normalizer = new ContentNormalizer();
DCN_RuntimeSettings settings;
int errorCode = normalizer->GetRuntimeSettings(&settings);
settings->scaleDownThreshold = 4096;
char errorMessage[256];
errorCode = normalizer->UpdateRuntimeSettings(&settings, errorMessage, 256);
delete normalizer;
```
