---
title: Procedimiento Llamar a un controlador de eventos en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- event handlers [Visual Basic], calling
- event handlers
- procedures [Visual Basic], event handlers
- procedures [Visual Basic], calling
ms.assetid: 72e18ef8-144e-40df-a1f4-066a57271e28
ms.openlocfilehash: 6fc08e9f16753dc853daff0120661603571d9db4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54717979"
---
# <a name="how-to-call-an-event-handler-in-visual-basic"></a>Procedimiento Llamar a un controlador de eventos en Visual Basic
Un *eventos* es una acción o aparición, como un mouse ha superado un límite de crédito o haga clic en, que es reconocido por algún componente del programa, y para el que puede escribir código para responder. Un *controlador de eventos* es el código que escribe para responder a un evento.  
  
 Un controlador de eventos en Visual Basic es un `Sub` procedimiento. Sin embargo, no normalmente se llama, la misma manera que otras `Sub` procedimientos. En su lugar, se identifica el procedimiento como un controlador para el evento. Puede hacerlo con un [controla](../../../../visual-basic/language-reference/statements/handles-clause.md) cláusula y un [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md) variable, o con un [AddHandler (instrucción)](../../../../visual-basic/language-reference/statements/addhandler-statement.md). Mediante un `Handles` cláusula es el modo predeterminado para declarar un controlador de eventos en Visual Basic. Esta es la manera en que los controladores de eventos se escriben los diseñadores al programar en el entorno de desarrollo integrado (IDE). El `AddHandler` instrucción es adecuada para generar eventos de forma dinámica en tiempo de ejecución.  
  
 Cuando se produce el evento, Visual Basic llama automáticamente al procedimiento del controlador de eventos. Cualquier código que tenga acceso a los eventos puede provocar que se produzcan al ejecutar un [RaiseEvent (instrucción)](../../../../visual-basic/language-reference/statements/raiseevent-statement.md).  
  
 Puede asociar más de un controlador de eventos con el mismo evento. En algunos casos puede desasociar un controlador de un evento. Para más información, vea [Eventos](../../../../visual-basic/programming-guide/language-features/events/index.md).  
  
### <a name="to-call-an-event-handler-using-handles-and-withevents"></a>Para llamar a un controlador de eventos con identificadores y WithEvents  
  
1.  Asegúrese de que el evento se declara con un [Event (instrucción)](../../../../visual-basic/language-reference/statements/event-statement.md).  
  
2.  Declare una variable de objeto en el módulo o clase de nivel, con el [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md) palabra clave. El `As` cláusula para esta variable debe especificar la clase que provoca el evento.  
  
3.  En la declaración de control de eventos `Sub` procedimiento, agregue un [controla](../../../../visual-basic/language-reference/statements/handles-clause.md) cláusula que especifica el `WithEvents` variable y el nombre del evento.  
  
4.  Cuando se produce el evento, Visual Basic llama automáticamente el `Sub` procedimiento. El código puede usar un `RaiseEvent` instrucción para hacer que se produzca el evento.  
  
     En el ejemplo siguiente se define un evento y un `WithEvents` variable que hace referencia a la clase que provoca el evento. El control de eventos `Sub` procedimiento usa un `Handles` cláusula para especificar la clase y que controla el evento.  
  
     [!code-vb[VbVbcnProcedures#4](./codesnippet/VisualBasic/how-to-call-an-event-handler_1.vb)]  
  
### <a name="to-call-an-event-handler-using-addhandler"></a>Para llamar a un controlador de eventos mediante AddHandler  
  
1.  Asegúrese de que el evento se declara con un `Event` instrucción.  
  
2.  Ejecutar un [AddHandler (instrucción)](../../../../visual-basic/language-reference/statements/addhandler-statement.md) para conectar de forma dinámica el control de eventos `Sub` procedimiento con el evento.  
  
3.  Cuando se produce el evento, Visual Basic llama automáticamente el `Sub` procedimiento. El código puede usar un `RaiseEvent` instrucción para hacer que se produzca el evento.  
  
     En el ejemplo siguiente se define un `Sub` procedimiento para controlar el <xref:System.Windows.Forms.Form.Closing> eventos de un formulario. A continuación, usa el [AddHandler (instrucción)](../../../../visual-basic/language-reference/statements/addhandler-statement.md) para asociar el `catchClose` procedimiento como un controlador de eventos <xref:System.Windows.Forms.Form.Closing>.  
  
     [!code-vb[VbVbcnProcedures#5](./codesnippet/VisualBasic/how-to-call-an-event-handler_2.vb)]  
  
     Puede desasociar un controlador de eventos a un evento mediante la ejecución de la [RemoveHandler (instrucción)](../../../../visual-basic/language-reference/statements/removehandler-statement.md).  
  
## <a name="see-also"></a>Vea también
- [Procedimientos](./index.md)
- [Subprocedimientos](./sub-procedures.md)
- [Sub (instrucción)](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [AddressOf (operador)](../../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Cómo: Crear un procedimiento](./how-to-create-a-procedure.md)
- [Cómo: Llamar a un procedimiento que no devuelve un valor](./how-to-call-a-procedure-that-does-not-return-a-value.md)
