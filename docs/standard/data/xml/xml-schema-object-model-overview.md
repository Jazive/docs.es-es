---
title: Información general sobre el Modelo de objetos de esquema XML
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 896a1e12-5655-42c6-8cdd-89c12862b34b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c63a21ed871bf967674d09230f897b7ab98dfa4d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554951"
---
# <a name="xml-schema-object-model-overview"></a>Información general sobre el Modelo de objetos de esquema XML
El Modelo de objetos de esquema (SOM) de Microsoft .NET Framework es una API enriquecida que le permite crear, editar y validar esquemas mediante programación. El SOM funciona en los documentos de esquemas XML de forma similar a cómo funciona el Modelo de objetos de documento (DOM) en los documentos XML. Los documentos de esquemas XML son archivos XML válidos que, una vez cargados en el SOM, transmiten significado sobre la estructura y la validez de otros documentos XML que cumplen el esquema.  
  
 Un esquema es un documento XML que define una clase de documentos XML especificando la estructura o el modelo de los documentos XML de un esquema en particular. Un esquema identifica las restricciones del contenido de los documentos XML y describe el vocabulario (reglas o gramática) que deben seguir los documentos conforme a XML para que se consideren válidos en ese esquema en particular. La validación de un documento XML es el proceso que garantiza que el documento sigue la gramática que especifica el esquema.  
  
 A continuación se indican las formas en las que la API del SOM de .NET Framework le permite crear, editar y validar esquemas.  
  
-   Cargue esquemas validos desde archivos y guárdelos en ellos.  
  
-   Cree esquemas en memoria utilizando clases fuertemente tipadas.  
  
-   Interactúe con la clase <xref:System.Xml.Schema.XmlSchemaSet> para guardar en caché, compilar y recuperar esquemas.  
  
-   Interactúe con el método <xref:System.Xml.XmlReader.Create%2A> de la clase <xref:System.Xml.XmlReader> para validar documentos de instancias XML con esquemas.  
  
-   Compile editores para crear y mantener esquemas.  
  
-   Edite dinámicamente un esquema que se pueda compilar y guardar para utilizarlo en la validación de documentos de instancias XML.  
  
## <a name="the-schema-object-model"></a>El Modelo de objetos de esquema  
 El SOM consta de un amplio conjunto de clases en el espacio de nombres <xref:System.Xml.Schema?displayProperty=nameWithType> que se corresponde a los elementos de un esquema XML. Por ejemplo, el elemento `<xsd:schema>...</xsd:schema>` se asigna a la clase <xref:System.Xml.Schema.XmlSchema?displayProperty=nameWithType> y toda la información que puede contener un elemento `<xsd:schema/>` se puede representar utilizando la clase <xref:System.Xml.Schema.XmlSchema>. Igualmente, los elementos `<xsd:element>...</xsd:element>` y `<xsd:attribute>...</xsd:attribute>` se asignan a las clases <xref:System.Xml.Schema.XmlSchemaElement?displayProperty=nameWithType> y <xref:System.Xml.Schema.XmlSchemaAttribute?displayProperty=nameWithType>, respectivamente. Esta asignación continúa para todos los elementos de un esquema XML que creen un Modelo de objetos de esquema XML en el espacio de nombres <xref:System.Xml.Schema>, tal y como se ilustra en el siguiente diagrama.  
  
 ![System.Xml.Schema Object Model](../../../../docs/standard/data/xml/media/xmlschemaobjmodeloverview.gif "XMLSchemaObjModelOverview")  
  
 Para obtener más información sobre cada clase del espacio de nombres <xref:System.Xml.Schema>, vea la documentación de referencia del espacio de nombres <xref:System.Xml.Schema> en la biblioteca de clases de .NET Framework.  
  
## <a name="see-also"></a>Vea también

- [Lectura y escritura de esquemas XML](../../../../docs/standard/data/xml/reading-and-writing-xml-schemas.md)
- [Compilación de esquemas XML](../../../../docs/standard/data/xml/building-xml-schemas.md)
- [Recorrido de esquemas XML](../../../../docs/standard/data/xml/traversing-xml-schemas.md)
- [Edición de esquemas XML](../../../../docs/standard/data/xml/editing-xml-schemas.md)
- [Inclusión o importación de esquemas XML](../../../../docs/standard/data/xml/including-or-importing-xml-schemas.md)
- [XmlSchemaSet para compilación de esquemas](../../../../docs/standard/data/xml/xmlschemaset-for-schema-compilation.md)
- [Conjunto de información posterior a la compilación de esquemas](../../../../docs/standard/data/xml/post-schema-compilation-infoset.md)
