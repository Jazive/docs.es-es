---
title: 'Tutorial: Actualizar la información de la barra de estado en tiempo de ejecución'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- status bars [Windows Forms], updating at run time
- status bars [Windows Forms], refreshing panels
- StatusBar control [Windows Forms], refreshing panels
- panels [Windows Forms], refreshing status bar
ms.assetid: cc2abb06-c082-49f7-a5a3-2fd1bbcb58d1
ms.openlocfilehash: 3de554d4c8c3963948159bc6b8c2196f9ebc10ad
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745888"
---
# <a name="walkthrough-updating-status-bar-information-at-run-time"></a>Tutorial: Actualizar la información de la barra de estado en tiempo de ejecución
> [!IMPORTANT]
>  El <xref:System.Windows.Forms.StatusStrip> y <xref:System.Windows.Forms.ToolStripStatusLabel> controles reemplazan y agregan funcionalidad a la <xref:System.Windows.Forms.StatusBar> y <xref:System.Windows.Forms.StatusBarPanel> controla; sin embargo, el <xref:System.Windows.Forms.StatusBar> y <xref:System.Windows.Forms.StatusBarPanel> controles se conservan por compatibilidad con versiones anteriores y uso futuro, si se Elija esta opción.  
  
 Con frecuencia, un programa llamará para que actualice el contenido de los paneles de la barra de estado dinámicamente en tiempo de ejecución, en función de los cambios de estado de la aplicación u otra interacción del usuario. Se trata de una manera habitual de indicar a los usuarios que teclas tales como Bloq Mayús, Bloq Num o BLOQ DESPL están habilitadas o para proporcionar la fecha o un reloj como referencia cómoda.  
  
 En el ejemplo siguiente, utilizará una instancia de la <xref:System.Windows.Forms.StatusBarPanel> clase para hospedar un reloj.  
  
### <a name="to-get-the-status-bar-ready-for-updating"></a>Para preparar la barra de estado para la actualización  
  
1.  Cree un nuevo formulario Windows Forms.  
  
2.  Agregue un control <xref:System.Windows.Forms.StatusBar> al formulario. Para obtener más información, vea [Cómo: Agregar controles a Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
3.  Agregar un panel de la barra de estado para su <xref:System.Windows.Forms.StatusBar> control. Para obtener más información, vea [Cómo: Agregar paneles a un Control StatusBar](../../../../docs/framework/winforms/controls/how-to-add-panels-to-a-statusbar-control.md).  
  
4.  Para el <xref:System.Windows.Forms.StatusBar> control agregado al formulario, establezca la <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> propiedad `true`.  
  
5.  Agregar un formulario Windows Forms <xref:System.Windows.Forms.Timer> componente al formulario.  
  
    > [!NOTE]
    >  Los formularios de Windows <xref:System.Windows.Forms.Timer?displayProperty=nameWithType> componente está diseñado para un entorno de Windows Forms. Si necesita un temporizador que sea adecuado para un entorno de servidor, consulte [Introducción a los temporizadores basados en servidor](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).  
  
6.  Establezca la propiedad <xref:System.Windows.Forms.Timer.Enabled%2A> en `true`.  
  
7.  Establecer el <xref:System.Windows.Forms.Timer.Interval%2A> propiedad de la <xref:System.Windows.Forms.Timer> en 30000.  
  
    > [!NOTE]
    >  El <xref:System.Windows.Forms.Timer.Interval%2A> propiedad de la <xref:System.Windows.Forms.Timer> componente se establece en 30 segundos (30.000 milisegundos) para asegurarse de que se refleja la hora exacta en la hora mostrada.  
  
### <a name="to-implement-the-timer-to-update-the-status-bar"></a>Para implementar el temporizador para que se actualice la barra de estado  
  
1.  Inserte el código siguiente en el controlador de eventos de la <xref:System.Windows.Forms.Timer> componente para actualizar el panel de la <xref:System.Windows.Forms.StatusBar> control.  
  
    ```vb  
    Private Sub Timer1_Tick(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Timer1.Tick  
       StatusBar1.Panels(0).Text = Now.ToShortTimeString  
    End Sub  
    ```  
  
    ```csharp  
    private void timer1_Tick(object sender, System.EventArgs e)  
    {  
       statusBar1.Panels[0].Text = DateTime.Now.ToShortTimeString();  
    }  
    ```  
  
    ```cpp  
    private:  
      System::Void timer1_Tick(System::Object ^ sender,  
        System::EventArgs ^ e)  
      {  
        statusBar1->Panels[0]->Text =  
          DateTime::Now.ToShortTimeString();  
      }  
    ```  
  
     Ahora está listo para ejecutar la aplicación y observar el reloj en ejecución en el panel de la barra de estado.  
  
### <a name="to-test-the-application"></a>Para probar la aplicación  
  
1.  Depure la aplicación y presione F5 para ejecutarla. Para más detalles sobre la depuración, consulte [Depurar en Visual Studio](/visualstudio/debugger/debugging-in-visual-studio).  
  
    > [!NOTE]
    >  El reloj tardará aproximadamente 30 segundos en aparecer en la barra de estado. El objetivo es obtener la hora más precisa posible. A la inversa, para que el reloj aparezca antes, puede reducir el valor de la <xref:System.Windows.Forms.Timer.Interval%2A> propiedad establecidos en el paso 7 del procedimiento anterior.  
  
## <a name="see-also"></a>Vea también
- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [Cómo: Agregar paneles a un Control StatusBar](../../../../docs/framework/winforms/controls/how-to-add-panels-to-a-statusbar-control.md)
- [Cómo: Determinar qué Panel de Control StatusBar de formularios Windows Forms se hizo clic](../../../../docs/framework/winforms/controls/determine-which-panel-wf-statusbar-control-was-clicked.md)
- [Información general sobre StatusBar (Control)](../../../../docs/framework/winforms/controls/statusbar-control-overview-windows-forms.md)
