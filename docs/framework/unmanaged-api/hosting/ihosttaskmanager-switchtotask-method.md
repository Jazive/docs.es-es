---
title: "IHostTaskManager::SwitchToTask (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostTaskManager.SwitchToTask
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostTaskManager::SwitchToTask
helpviewer_keywords:
- IHostTaskManager::SwitchToTask method [.NET Framework hosting]
- SwitchToTask method [.NET Framework hosting]
ms.assetid: 35d0c27e-4b14-49ce-810d-7ab2120177e8
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 9b85c762bd2d10baddfa013a8310e3b542a94af6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="ihosttaskmanagerswitchtotask-method"></a><span data-ttu-id="e8eda-102">IHostTaskManager::SwitchToTask (Método)</span><span class="sxs-lookup"><span data-stu-id="e8eda-102">IHostTaskManager::SwitchToTask Method</span></span>
<span data-ttu-id="e8eda-103">Notifica al host que debe cambiar la tarea actual.</span><span class="sxs-lookup"><span data-stu-id="e8eda-103">Notifies the host that it should switch out the current task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8eda-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8eda-104">Syntax</span></span>  
  
```  
HRESULT SwitchToTask (  
    [in] DWORD option  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8eda-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8eda-105">Parameters</span></span>  
 `option`  
 <span data-ttu-id="e8eda-106">[in] Uno de los [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) valores de enumeración, que indica la acción que debe realizar el host si bloquea la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="e8eda-106">[in] One of the [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) enumeration values, indicating the action the host should take if the requested operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e8eda-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8eda-107">Return Value</span></span>  
  
|<span data-ttu-id="e8eda-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e8eda-108">HRESULT</span></span>|<span data-ttu-id="e8eda-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8eda-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e8eda-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8eda-110">S_OK</span></span>|<span data-ttu-id="e8eda-111">`SwitchToTask`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8eda-111">`SwitchToTask` returned successfully.</span></span>|  
|<span data-ttu-id="e8eda-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e8eda-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e8eda-113">Common language runtime (CLR) no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8eda-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e8eda-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e8eda-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e8eda-115">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="e8eda-115">The call timed out.</span></span>|  
|<span data-ttu-id="e8eda-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e8eda-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e8eda-117">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="e8eda-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e8eda-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e8eda-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e8eda-119">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="e8eda-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e8eda-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e8eda-120">E_FAIL</span></span>|<span data-ttu-id="e8eda-121">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="e8eda-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e8eda-122">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="e8eda-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e8eda-123">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e8eda-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e8eda-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8eda-124">Remarks</span></span>  
 <span data-ttu-id="e8eda-125">El host puede cambiar a otra tarea si fuera necesario.</span><span class="sxs-lookup"><span data-stu-id="e8eda-125">The host can switch in another task as desired or needed.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e8eda-126">`SwitchToTask`no especifica qué tareas debe cambiar el host especifica solo a la tarea que debe realizar el cambio de.</span><span class="sxs-lookup"><span data-stu-id="e8eda-126">`SwitchToTask` does not specify which task the host should switch to; it specifies only the task that it should switch from.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8eda-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8eda-127">Requirements</span></span>  
 <span data-ttu-id="e8eda-128">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8eda-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8eda-129">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e8eda-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e8eda-130">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e8eda-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e8eda-131">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8eda-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8eda-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8eda-132">See Also</span></span>  
 [<span data-ttu-id="e8eda-133">ICLRTask (interfaz)</span><span class="sxs-lookup"><span data-stu-id="e8eda-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="e8eda-134">ICLRTaskManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="e8eda-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="e8eda-135">IHostTask (interfaz)</span><span class="sxs-lookup"><span data-stu-id="e8eda-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="e8eda-136">IHostTaskManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="e8eda-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)