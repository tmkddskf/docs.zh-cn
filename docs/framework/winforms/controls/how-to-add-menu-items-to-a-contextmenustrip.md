---
title: 如何：向 ContextMenuStrip 添加菜单项
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrips [Windows Forms], adding menu items
- shortcut menus [Windows Forms], adding items
- context menus [Windows Forms], adding menu items
ms.assetid: 1ec14776-3ea2-4752-bd22-4fae0fd19e1a
ms.openlocfilehash: d044cf92cf7ce6db3425aacf397d6c7b4f111324
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524620"
---
# <a name="how-to-add-menu-items-to-a-contextmenustrip"></a>如何：向 ContextMenuStrip 添加菜单项
可以将一个菜单项或多个项添加到的一次<xref:System.Windows.Forms.ContextMenuStrip>。  
  
### <a name="to-add-a-single-menu-item-to-a-contextmenustrip"></a>若要向 ContextMenuStrip 添加一个菜单项  
  
-   使用<xref:System.Windows.Forms.ToolStripItemCollection.Add%2A>方法将添加到的一个菜单项<xref:System.Windows.Forms.ContextMenuStrip>。  
  
    ```vb  
    Me.contextMenuStrip1.Items.Add(Me.toolStripMenuItem1)  
    ```  
  
    ```csharp  
    this.contextMenuStrip1.Items.Add(toolStripMenuItem1);  
    ```  
  
### <a name="to-add-several-menu-items-to-a-contextmenustrip"></a>若要向 ContextMenuStrip 添加多个菜单项  
  
-   使用<xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A>方法将添加到多个菜单项<xref:System.Windows.Forms.ContextMenuStrip>。  
  
    ```vb  
    Me.contextMenuStrip1.Items.AddRange(New _  
       System.Windows.Forms.ToolStripItem() {Me.toolStripMenuItem1, _  
          Me.toolStripMenuItem2})  
    ```  
  
    ```csharp  
    this.contextMenuStrip1.Items.AddRange(new   
       System.Windows.Forms.ToolStripItem[] {  
          this.toolStripMenuItem1, this.toolStripMenuItem2});  
    ```  
  
## <a name="see-also"></a>请参阅  
 [ContextMenuStrip 控件](../../../../docs/framework/winforms/controls/contextmenustrip-control.md)
