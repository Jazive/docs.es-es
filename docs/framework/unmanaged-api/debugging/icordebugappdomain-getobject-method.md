---
title: ICorDebugAppDomain::GetObject (Método)
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetObject
api_location:
- corguids.lib
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetObject
helpviewer_keywords:
- ICorDebugAppDomain::GetObject method [.NET Framework debugging]
- GetObject method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 78232e6f-ae18-4cfa-a6cd-e79471cf9d76
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a6f528bcef7d06b503b1ee9d7bd4a61d3d3e9672
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406525"
---
# <a name="icordebugappdomaingetobject-method"></a>ICorDebugAppDomain::GetObject (Método)
Obtiene un puntero de interfaz al dominio de aplicación de common language runtime (CLR).  
  
## <a name="syntax"></a>Sintaxis  
  
```  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `ppObject`  
 [out] Un puntero a la dirección de un objeto de interfaz de ICorDebugValue que representa el dominio de aplicación de CLR.  
  
## <a name="return-value"></a>Valor devuelto  
 Si un administrados <xref:System.AppDomain?displayProperty=nameWithType> no se ha construido el objeto para este dominio de aplicación, el método devuelve `S_FALSE` y lo coloca `NULL` en `*ppObject`.  
  
## <a name="remarks"></a>Comentarios  
 Cada dominio de aplicación en un proceso puede tener un administrado <xref:System.AppDomain?displayProperty=nameWithType> objeto en el tiempo de ejecución que lo representa. Esta función obtiene un objeto de interfaz de ICorDebugValue que corresponde a este administrado <xref:System.AppDomain?displayProperty=nameWithType> objeto.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado:** CorDebug.idl, CorDebug.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **Versiones de .NET framework:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]
