---
title: Filtrar Habilitar la vista en mosaico en un Control de ListView de Windows Forms mediante el diseñador
ms.date: 03/30/2017
helpviewer_keywords:
- tile view feature
- ListView control [Windows Forms], tile view
- tiling [Windows Forms], Windows Forms, controls
ms.assetid: 12f0816a-52b8-41ee-a6d9-ded3a8a5817a
ms.openlocfilehash: 0acd235fe015b3f93364482b83008b388c1b86d9
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303977"
---
# <a name="how-to-enable-tile-view-in-a-windows-forms-listview-control-using-the-designer"></a>Filtrar Habilitar la vista en mosaico en un Control de ListView de Windows Forms mediante el diseñador
La característica de vista de mosaico de la <xref:System.Windows.Forms.ListView> control le permite proporcionar equilibrio visual entre la información gráfica y textual. La información de texto que se muestra para un elemento en la vista de mosaico es igual que la información de columna definida para la vista de detalles. Vista en mosaico funciona en combinación con la agrupación o la inserción marca las características de la <xref:System.Windows.Forms.ListView> control.  
  
 La vista de mosaico usa una imagen 32 x 32 y varias líneas de texto, como se muestra en la siguiente imagen.  
  
 ![Vista en mosaico en un Control ListView](../../../../docs/framework/winforms/controls/media/listviewtile.gif "ListViewTile")  
  
 Icono Vista de propiedades y métodos permiten especificar qué campos de columna para mostrar para cada elemento y controlar colectivamente el tamaño y la apariencia de todos los elementos dentro de una ventana de vista de mosaico. Para mayor claridad, la primera línea del texto de un mosaico siempre es el nombre del elemento; no se puede cambiar.  
  
 El procedimiento siguiente requiere una **aplicación Windows** proyecto con un formulario que contenga un <xref:System.Windows.Forms.ListView> control. Para obtener información acerca de cómo configurar un proyecto de este tipo, vea [Cómo: Cree un proyecto de aplicación de Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) y [Cómo: Agregar controles a Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  La vista de mosaico solo está disponible en [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] cuando la aplicación llama al método <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>. En sistemas operativos anteriores, el código relacionado con la vista de mosaico no tiene ningún efecto y el control <xref:System.Windows.Forms.ListView> se muestra en la vista de iconos grandes. Para obtener más información, consulta <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.  
>   
>  Los cuadros de diálogo y comandos de menú que se ven pueden diferir de los descritos en la Ayuda, en función de los valores de configuración o de edición activos. Para cambiar la configuración, elija la opción **Importar y exportar configuraciones** del menú **Herramientas** . Para más información, vea [Personalizar el IDE de Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-set-tile-view-in-the-designer"></a>Para establecer la vista en mosaico en el diseñador  
  
1.  Seleccione el <xref:System.Windows.Forms.ListView> control en el formulario.  
  
2.  En el **propiedades** ventana, seleccione el <xref:System.Windows.Forms.ListView.View%2A> propiedad y elija **icono**.  
  
## <a name="see-also"></a>Vea también
- <xref:System.Windows.Forms.ListView.TileSize%2A>
- [Información general del control ListView](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
