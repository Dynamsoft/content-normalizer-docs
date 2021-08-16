---
title: Dynamsoft Content Normalizer Parameter Reference - MinimalVerticalSideLength
keywords: minimalverticalsidelength, parameters, reference, dcn, documentation
description: Dynamsoft Content Normalizer Parameter Reference - MinimalVerticalSideLength
needGenerateH3Content: true
---


# MinimalVerticalSideLength
Sets the minimal vertical side length of the quadrilateral. 

## Setting Methods
### As Json Parameter

| Parent Json Object | Json Parameter Name | Value Type | 
| ------------------ | ------------------- | ---------- |
| ContentNormalizerParameter | MinimalVerticalSideLength | *int array* |

**Value Range**    
    Format: [`minimalSideLength`, `ByPercentage`]    
    Allowed value range:   
        &emsp;&emsp;For `minimalSideLength`: `ByPercentage`=0: [1, 0x7fffffff], `ByPercentage`=1: [1, 100]   
        &emsp;&emsp;For `ByPercentage`: [0, 1]   

**Default Value**   
    [15, 1]

**Example**  
```json
{
    "MinimalVerticalSideLength": [200, 0],
}
```

### As Struct Member

| Struct | Struct Member Name | Value Type | 
| ------ | ------------------ | ---------- |
| DCN_RuntimeSettings | minimalVerticalSideLength | *int array* |

**Value Range**    
    Format: [`minimalSideLength`, `ByPercentage`]    
    Allowed value range:   
        &emsp;&emsp;For `minimalSideLength`: `ByPercentage`=0: [1, 0x7fffffff], `ByPercentage`=1: [1, 100]   
        &emsp;&emsp;For `ByPercentage`: [0, 1]   

**Default Value**   
    [15, 1]

**Code Snippet**  
```cpp
// This is a c++ sample code.
ContentNormalizer::InitLicense("t0260NwAAAHV***************");
ContentNormalizer* normalizer = new ContentNormalizer();
DCN_RuntimeSettings settings;
int errorCode = normalizer->GetRuntimeSettings(&settings);
settings->minimalVerticalSideLength[0] = 200;
settings->minimalVerticalSideLength[1] = 0;
char errorMessage[256];
errorCode = normalizer->UpdateRuntimeSettings(&settings, errorMessage, 256);
delete normalizer;
```
