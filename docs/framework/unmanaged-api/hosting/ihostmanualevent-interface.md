---
title: IHostManualEvent (Interfaz)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostManualEvent
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostManualEvent
helpviewer_keywords: IHostManualEvent interface [.NET Framework hosting]
ms.assetid: 300c2661-b7d1-4c39-b080-9ebdef0fd523
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5c19125d96d5f4a9e91fc083d53f36ebebd2c569
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="ihostmanualevent-interface"></a><span data-ttu-id="822fa-102">IHostManualEvent (Interfaz)</span><span class="sxs-lookup"><span data-stu-id="822fa-102">IHostManualEvent Interface</span></span>
<span data-ttu-id="822fa-103">Proporciona la implementación del host de una representación de un evento de restablecimiento manual.</span><span class="sxs-lookup"><span data-stu-id="822fa-103">Provides the host's implementation of a representation of a manual reset event.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="822fa-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="822fa-104">Methods</span></span>  
  
|<span data-ttu-id="822fa-105">Método</span><span class="sxs-lookup"><span data-stu-id="822fa-105">Method</span></span>|<span data-ttu-id="822fa-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="822fa-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="822fa-107">Reset (método)</span><span class="sxs-lookup"><span data-stu-id="822fa-107">Reset Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-reset-method.md)|<span data-ttu-id="822fa-108">Restablece el actual `IHostManualEvent` instancia a un estado no señalado.</span><span class="sxs-lookup"><span data-stu-id="822fa-108">Resets the current `IHostManualEvent` instance to a non-signaled state.</span></span>|  
|[<span data-ttu-id="822fa-109">Set (método)</span><span class="sxs-lookup"><span data-stu-id="822fa-109">Set Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-set-method.md)|<span data-ttu-id="822fa-110">Establece la actual `IHostManualEvent` instancia en un estado señalado.</span><span class="sxs-lookup"><span data-stu-id="822fa-110">Sets the current `IHostManualEvent` instance to a signaled state.</span></span>|  
|[<span data-ttu-id="822fa-111">Wait (método)</span><span class="sxs-lookup"><span data-stu-id="822fa-111">Wait Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-wait-method.md)|<span data-ttu-id="822fa-112">Hace que el actual `IHostManualEvent` instancia espere hasta que encuentre un propietario o una cantidad especificada de tiempo determinado.</span><span class="sxs-lookup"><span data-stu-id="822fa-112">Causes the current `IHostManualEvent` instance to wait until it is owned, or a specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="822fa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="822fa-113">Requirements</span></span>  
 <span data-ttu-id="822fa-114">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="822fa-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="822fa-115">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="822fa-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="822fa-116">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="822fa-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="822fa-117">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="822fa-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="822fa-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="822fa-118">See Also</span></span>  
 [<span data-ttu-id="822fa-119">ICLRSyncManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="822fa-119">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="822fa-120">IHostAutoEvent (interfaz)</span><span class="sxs-lookup"><span data-stu-id="822fa-120">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)  
 [<span data-ttu-id="822fa-121">IHostSemaphore (interfaz)</span><span class="sxs-lookup"><span data-stu-id="822fa-121">IHostSemaphore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md)  
 [<span data-ttu-id="822fa-122">IHostSyncManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="822fa-122">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)  
 [<span data-ttu-id="822fa-123">Interfaces de hospedaje</span><span class="sxs-lookup"><span data-stu-id="822fa-123">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)