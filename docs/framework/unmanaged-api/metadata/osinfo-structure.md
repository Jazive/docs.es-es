---
title: OSINFO (Estructura)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: OSINFO
api_location: mscoree.dll
api_type: COM
f1_keywords: OSINFO
helpviewer_keywords: OSINFO structure [.NET Framework metadata]
ms.assetid: fac7b480-7adb-4450-a5e9-690fed81ffae
topic_type: apiref
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 700e9bcfe33e5be3725bd24b212b3a77ad139b2c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="osinfo-structure"></a><span data-ttu-id="717d5-102">OSINFO (Estructura)</span><span class="sxs-lookup"><span data-stu-id="717d5-102">OSINFO Structure</span></span>
<span data-ttu-id="717d5-103">Contiene detalles sobre el sistema operativo para un ensamblado o módulo.</span><span class="sxs-lookup"><span data-stu-id="717d5-103">Contains details about the operating system for an assembly or module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="717d5-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="717d5-104">Syntax</span></span>  
  
```  
typedef struct {  
    DWORD   dwOSPlatformId;  
    DWORD   dwOSMajorVersion;   
    DWORD   dwOSMinorVersion;   
} OSINFO;  
```  
  
## <a name="members"></a><span data-ttu-id="717d5-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="717d5-105">Members</span></span>  
  
|<span data-ttu-id="717d5-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="717d5-106">Member</span></span>|<span data-ttu-id="717d5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="717d5-107">Description</span></span>|  
|------------|-----------------|  
|`dwOSPlatformId`|<span data-ttu-id="717d5-108">Uno de los valores de identificador definidos por la función de la plataforma de Microsoft Windows `GetVersionEx`.</span><span class="sxs-lookup"><span data-stu-id="717d5-108">One of the identifier values defined by the Microsoft Windows platform function `GetVersionEx`.</span></span> <span data-ttu-id="717d5-109">Se admiten los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="717d5-109">The following values are supported:</span></span><br /><br /> <span data-ttu-id="717d5-110">-VER_PLATFORM_WIN32s, o 0 x 0000, para especificar Microsoft Windows 3.1.</span><span class="sxs-lookup"><span data-stu-id="717d5-110">-   VER_PLATFORM_WIN32s, or 0x0000, to specify Microsoft Windows 3.1.</span></span><br /><span data-ttu-id="717d5-111">-VER_PLATFORM_WIN32_WINDOWS, o 0 x 0001, para especificar Windows 95, Windows 98 o sistemas operativos descendientes de ellos.</span><span class="sxs-lookup"><span data-stu-id="717d5-111">-   VER_PLATFORM_WIN32_WINDOWS, or 0x0001, to specify Windows 95, Windows 98, or operating systems descended from them.</span></span><br /><span data-ttu-id="717d5-112">-VER_PLATFORM_WIN32_NT, o 0 x 0010, para especificar Windows NT o sistemas operativos descendientes de él.</span><span class="sxs-lookup"><span data-stu-id="717d5-112">-   VER_PLATFORM_WIN32_NT, or 0x0010, to specify Windows NT or operating systems descended from it.</span></span>|  
|`dwOSMajorVersion`|<span data-ttu-id="717d5-113">La versión principal del sistema operativo, o un valor NULL para indicar cualquier versión.</span><span class="sxs-lookup"><span data-stu-id="717d5-113">The operating system major version, or a NULL value to indicate any version.</span></span>|  
|`dwOSMinorVersion`|<span data-ttu-id="717d5-114">La versión secundaria del sistema operativo, o un valor NULL para indicar cualquier versión.</span><span class="sxs-lookup"><span data-stu-id="717d5-114">The operating system minor version, or a NULL value to indicate any version.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="717d5-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="717d5-115">Remarks</span></span>  
 <span data-ttu-id="717d5-116">`OSINFO`se basa en el `OSVERSIONINFOEX` estructura que es usan en las llamadas a la función de la plataforma de Microsoft Windows `GetVersionEx`.</span><span class="sxs-lookup"><span data-stu-id="717d5-116">`OSINFO` is based on the `OSVERSIONINFOEX` structure that is used in calls to the Microsoft Windows platform function `GetVersionEx`.</span></span> <span data-ttu-id="717d5-117">Esta estructura se utiliza por ASSEMBLYMETADATA (estructura) para indicar su compatibilidad de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="717d5-117">This structure is used by the ASSEMBLYMETADATA structure to indicate its operating system support.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="717d5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="717d5-118">Requirements</span></span>  
 <span data-ttu-id="717d5-119">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="717d5-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="717d5-120">**Encabezado:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="717d5-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="717d5-121">**Biblioteca:** usada como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="717d5-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="717d5-122">**Versiones de .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="717d5-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="717d5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="717d5-123">See Also</span></span>  
 [<span data-ttu-id="717d5-124">Estructuras de metadatos</span><span class="sxs-lookup"><span data-stu-id="717d5-124">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)  
 [<span data-ttu-id="717d5-125">IMetaDataAssemblyEmit (interfaz)</span><span class="sxs-lookup"><span data-stu-id="717d5-125">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)