---
title: ICorDebugManagedCallback2::ChangeConnection 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.ChangeConnection
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::ChangeConnection
helpviewer_keywords:
- ICorDebugManagedCallback2::ChangeConnection method [.NET Framework debugging]
- ChangeConnection method [.NET Framework debugging]
ms.assetid: 7263f9a9-4c0b-4d82-a181-288873fb2b18
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 68288111e3f862cf1364031eaad9c63cf347146f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415933"
---
# <a name="icordebugmanagedcallback2changeconnection-method"></a>ICorDebugManagedCallback2::ChangeConnection 方法
通知调试器与指定连接关联的任务组已更改。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT ChangeConnection (  
    [in] ICorDebugProcess     *pProcess,  
    [in] CONNID               dwConnectionId  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pProcess`  
 [in]指向一个表示包含更改连接的过程的"ICorDebugProcess"对象的指针。  
  
 `dwConnectionId`  
 [in]更改连接的 ID。  
  
## <a name="remarks"></a>备注  
 A`ChangeConnection`回调将触发在以下情况：  
  
-   当调试器附加到进程，其中包含连接。 在这种情况下，运行时将生成并调度[icordebugmanagedcallback2:: Createconnection](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-createconnection-method.md)事件和一个`ChangeConnection`事件过程中每个连接。 A`ChangeConnection`对于每个现有的连接，而不考虑该连接组的任务具有已更改其创建后生成事件。  
  
-   当主机调用[iclrdebugmanager:: Setconnectiontasks](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setconnectiontasks-method.md)中[承载 API](../../../../docs/framework/unmanaged-api/hosting/index.md)。  
  
 调试器应扫描以拾取新的更改的过程中的所有线程。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorDebug.idl、 CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [ICorDebugManagedCallback2 接口](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)  
 [ICorDebugManagedCallback 接口](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
