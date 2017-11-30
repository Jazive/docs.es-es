---
title: "ICLRDebugManager::SetConnectionTasks (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDebugManager.SetConnectionTasks
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRDebugManager::SetConnectionTasks
helpviewer_keywords:
- SetConnectionTasks method [.NET Framework hosting]
- ICLRDebugManager::SetConnectionTasks method [.NET Framework hosting]
ms.assetid: b38bbc9a-872c-41a9-b8c3-ca011d25456a
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 354e876bf69a82bf1eb0ed3907a03e4b94d60f19
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iclrdebugmanagersetconnectiontasks-method"></a><span data-ttu-id="227e7-102">ICLRDebugManager::SetConnectionTasks (Método)</span><span class="sxs-lookup"><span data-stu-id="227e7-102">ICLRDebugManager::SetConnectionTasks Method</span></span>
<span data-ttu-id="227e7-103">Asocia una lista de [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instancias con un identificador y un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="227e7-103">Associates a list of [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instances with an identifier and a friendly name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="227e7-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="227e7-104">Syntax</span></span>  
  
```  
HRESULT SetConnectionTasks (  
    [in] CONNID id,  
    [in] DWORD dwCount,  
    [in, size_is(dwCount)] ICLRTask **ppCLRTask  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="227e7-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="227e7-105">Parameters</span></span>  
 `id`  
 <span data-ttu-id="227e7-106">[in] El identificador específico del host para la conexión con la que se va a asociar el `ppCLRTask` matriz.</span><span class="sxs-lookup"><span data-stu-id="227e7-106">[in] The host-specific identifier for the connection with which to associate the `ppCLRTask` array.</span></span>  
  
 `dwCount`  
 <span data-ttu-id="227e7-107">[in] El número de miembros de `ppCLRTask`.</span><span class="sxs-lookup"><span data-stu-id="227e7-107">[in] The number of members of `ppCLRTask`.</span></span> <span data-ttu-id="227e7-108">Este número debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="227e7-108">This number must be greater than zero.</span></span>  
  
 `ppCLRTask`  
 <span data-ttu-id="227e7-109">[in] Una matriz de `ICLRTask` punteros para asociar a la conexión identificada por `id`.</span><span class="sxs-lookup"><span data-stu-id="227e7-109">[in] An array of `ICLRTask` pointers to associate with the connection identified by `id`.</span></span> <span data-ttu-id="227e7-110">Esta matriz debe contener a al menos un miembro.</span><span class="sxs-lookup"><span data-stu-id="227e7-110">This array must contain at least one member.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="227e7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="227e7-111">Return Value</span></span>  
  
|<span data-ttu-id="227e7-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="227e7-112">HRESULT</span></span>|<span data-ttu-id="227e7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="227e7-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="227e7-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="227e7-114">S_OK</span></span>|<span data-ttu-id="227e7-115">`SetConnectionTasks`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="227e7-115">`SetConnectionTasks` returned successfully.</span></span>|  
|<span data-ttu-id="227e7-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="227e7-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="227e7-117">Common language runtime (CLR) no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="227e7-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="227e7-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="227e7-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="227e7-119">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="227e7-119">The call timed out.</span></span>|  
|<span data-ttu-id="227e7-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="227e7-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="227e7-121">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="227e7-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="227e7-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="227e7-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="227e7-123">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="227e7-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="227e7-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="227e7-124">E_FAIL</span></span>|<span data-ttu-id="227e7-125">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="227e7-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="227e7-126">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="227e7-126">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="227e7-127">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="227e7-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="227e7-128">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="227e7-128">E_INVALIDARG</span></span>|<span data-ttu-id="227e7-129">[BeginConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md) no se ha llamado utilizando este valor de `id`, o `dwCount` o `id` es cero o uno de los elementos de `ppCLRTask` es null.</span><span class="sxs-lookup"><span data-stu-id="227e7-129">[BeginConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md) has not been called using this value of `id`, or `dwCount` or `id` is zero, or one of the elements of `ppCLRTask` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="227e7-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="227e7-130">Remarks</span></span>  
 <span data-ttu-id="227e7-131">[ICLRDebugManager](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md) proporciona tres métodos, `BeginConnection`, `SetConnectionTasks`, y [EndConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-endconnection-method.md), para asociar listas de tareas con identificadores y nombres descriptivos.</span><span class="sxs-lookup"><span data-stu-id="227e7-131">[ICLRDebugManager](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md) provides three methods, `BeginConnection`, `SetConnectionTasks`, and [EndConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-endconnection-method.md), for associating task lists with identifiers and friendly names.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="227e7-132">Estos tres métodos deben llamarse en un orden específico para cada conjunto de tareas.</span><span class="sxs-lookup"><span data-stu-id="227e7-132">These three methods must be called in a specific order for each set of tasks.</span></span> <span data-ttu-id="227e7-133">`BeginConnection`se llama en primer lugar para establecer una nueva conexión.</span><span class="sxs-lookup"><span data-stu-id="227e7-133">`BeginConnection` is called first to establish a new connection.</span></span> <span data-ttu-id="227e7-134">`SetConnectionTasks`se llama a continuación para proporcionar el conjunto de tareas que se asociará con esa conexión.</span><span class="sxs-lookup"><span data-stu-id="227e7-134">`SetConnectionTasks` is called next to provide the set of tasks to be associated with that connection.</span></span> <span data-ttu-id="227e7-135">`EndConnection`se llama última para quitar la asociación entre la lista de tareas y el identificador y el nombre descriptivo. Sin embargo, se pueden anidar las llamadas para conexiones diferentes.</span><span class="sxs-lookup"><span data-stu-id="227e7-135">`EndConnection` is called last to remove the association between the task list and the identifier and friendly name.However, calls for different connections can be nested.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="227e7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="227e7-136">Requirements</span></span>  
 <span data-ttu-id="227e7-137">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="227e7-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="227e7-138">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="227e7-138">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="227e7-139">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="227e7-139">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="227e7-140">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="227e7-140">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="227e7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="227e7-141">See Also</span></span>  
 [<span data-ttu-id="227e7-142">ICLRControl (interfaz)</span><span class="sxs-lookup"><span data-stu-id="227e7-142">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="227e7-143">ICLRDebugManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="227e7-143">ICLRDebugManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md)  
 [<span data-ttu-id="227e7-144">BeginConnection (método)</span><span class="sxs-lookup"><span data-stu-id="227e7-144">BeginConnection Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md)  
 [<span data-ttu-id="227e7-145">EndConnection (método)</span><span class="sxs-lookup"><span data-stu-id="227e7-145">EndConnection Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-endconnection-method.md)  
 [<span data-ttu-id="227e7-146">IHostControl (interfaz)</span><span class="sxs-lookup"><span data-stu-id="227e7-146">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)