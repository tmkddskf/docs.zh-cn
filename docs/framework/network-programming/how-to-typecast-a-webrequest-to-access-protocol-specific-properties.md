---
title: 如何：转换 WebRequest 以访问特定于协议的属性
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d9a8eae2-7454-46f9-b43b-c98477c5bcde
ms.openlocfilehash: ec5b9f1db17cf1c90484b0a44063efef9fa16cf9
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2018
ms.locfileid: "50180083"
---
# <a name="how-to-typecast-a-webrequest-to-access-protocol-specific-properties"></a>如何：转换 WebRequest 以访问特定于协议的属性
此示例演示如何类型转换 WebRequest 以访问特定于协议的属性。  
  
## <a name="example"></a>示例  
  
```csharp  
HttpWebRequest httpreq =   
   (HttpWebRequest) WebRequest.Create("http://www.contoso.com/");  
```  
  
```vb  
Dim httpreq As HttpWebRequest = _  
   CType(WebRequest.Create("http://www.contoso.com/"), HttpWebRequest)  
```  
  
## <a name="see-also"></a>请参阅  
 [对可插入协议进行编程](../../../docs/framework/network-programming/programming-pluggable-protocols.md)
