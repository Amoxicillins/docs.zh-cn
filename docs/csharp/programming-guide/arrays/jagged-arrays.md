---
title: 交错数组 - C# 编程指南
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- jagged arrays [C#]
- arrays [C#], jagged
ms.assetid: 537c65a6-0e0a-4a00-a2b8-086f38519c70
ms.openlocfilehash: f517a9a6d6e10f04df70729fb9e641c1f955f28a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237852"
---
# <a name="jagged-arrays-c-programming-guide"></a>交错数组（C# 编程指南）

交错数组是元素为数组的数组。 交错数组元素的维度和大小可以不同。 交错数组有时称为“数组的数组”。 以下示例说明如何声明、初始化和访问交错数组。  
  
 下面声明一个具有三个元素的一维数组，其中每个元素都是一维整数数组：  
  
 [!code-csharp[csProgGuideArrays#19](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_1.cs)]  
  
 必须初始化 `jaggedArray` 的元素后才可使用它。 可按下方操作初始化元素：  
  
 [!code-csharp[csProgGuideArrays#20](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_2.cs)]  
  
 每个元素都是一维整数数组。 第一个元素是由 5 个整数组成的数组，第二个是由 4 个整数组成的数组，而第三个是由 2 个整数组成的数组。  
  
 也可使用初始化表达式通过值来填充数组元素，这种情况下不需要数组大小。 例如:  
  
 [!code-csharp[csProgGuideArrays#21](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_3.cs)]  
  
 还可在声明数组时将其初始化，如：  
  
 [!code-csharp[csProgGuideArrays#22](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_4.cs)]  
  
 可以使用下面的缩写形式。 请注意：不能从元素初始化中省略 `new` 运算符，因为不存在元素的默认初始化：  
  
 [!code-csharp[csProgGuideArrays#23](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_5.cs)]  
  
 交错数组是数组的数组，因此其元素为引用类型且被初始化为 `null`。  
  
 可以如下例所示访问个别数组元素：  
  
 [!code-csharp[csProgGuideArrays#24](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_6.cs)]  
  
 可以混合使用交错数组和多维数组。 下面声明和初始化一个包含大小不同的三个二维数组元素的一维交错数组。 有关二维数组的详细信息，请参阅[多维数组](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)。  
  
 [!code-csharp[csProgGuideArrays#25](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_7.cs)]  
  
 可以如本例所示访问个别元素，示例显示第一个数组的元素 `[1,0]` 的值（值为 `5`）：  
  
 [!code-csharp[csProgGuideArrays#26](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_8.cs)]  
  
 方法 `Length` 返回包含在交错数组中的数组的数目。 例如，假定已声明了前一个数组，则此行：  
  
 [!code-csharp[csProgGuideArrays#27](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_9.cs)]  
  
 返回值 3。  
  
## <a name="example"></a>示例

 本例生成一个数组，该数组的元素为数组自身。 每一个数组元素都有不同的大小。  
  
 [!code-csharp[csProgGuideArrays#18](../../../csharp/programming-guide/arrays/codesnippet/CSharp/jagged-arrays_10.cs)]  
  
## <a name="see-also"></a>请参阅

- <xref:System.Array>  
- [C# 编程指南](../../../csharp/programming-guide/index.md)  
- [数组](../../../csharp/programming-guide/arrays/index.md)  
- [一维数组](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)  
- [多维数组](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)
