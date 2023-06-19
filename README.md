# ObiXcode15BuildTest
ObiXcode15BuildTest


Obi got a runtime error on ios devices when the app is Compile and build on xcode 15.
Product work fine under the same system setting when using xcode 14.3

ystem：MacOS 13.4
Devices M1 chip Macbook
Unity Version: 2021.3.11 & 2021.3.21
Obi Version : lastest

Use Xcode 15 build on iOS 16.3
Please see this video:
Compile is fine but runtime got error：
https://github.com/Cstedmund/ObiXcode15BuildTest/assets/92370517/b946bcb2-5190-4a02-9a62-d96d0d1ab6ab

Error log:
```
Lost connection to the debugger on “Chi Shing’s iPhone”.
Domain: IDEDebugSessionErrorDomain
Code: 22
Recovery Suggestion: Restore the connection to “Chi Shing’s iPhone” and run “Myproject” again, or if “Myproject” is still running, you can attach to it by selecting Debug > Attach to Process > Myproject.
User Info: {
    DVTErrorCreationDateKey = "2023-06-17 10:19:16 +0000";
    IDERunOperationFailingWorker = DBGLLDBLauncher;
}
--

Event Metadata: com.apple.dt.IDERunOperationWorkerFinished : {
    "device_model" = "iPhone14,6";
    "device_osBuild" = "16.3 (20D47)";
    "device_platform" = "com.apple.platform.iphoneos";
    "dvt_coredevice_version" = "325.3";
    "dvt_mobiledevice_version" = "1643.0.10.100.2";
    "launchSession_schemeCommand" = Run;
    "launchSession_state" = 2;
    "launchSession_targetArch" = arm64;
    "operation_duration_ms" = 15568;
    "operation_errorCode" = 22;
    "operation_errorDomain" = IDEDebugSessionErrorDomain;
    "operation_errorWorker" = DBGLLDBLauncher;
    "operation_name" = IDEiPhoneRunOperationWorkerGroup;
    "param_consoleMode" = 0;
    "param_debugger_attachToExtensions" = 0;
    "param_debugger_attachToXPC" = 0;
    "param_debugger_type" = 5;
    "param_destination_isProxy" = 0;
    "param_destination_platform" = "com.apple.platform.iphoneos";
    "param_diag_MainThreadChecker_stopOnIssue" = 0;
    "param_diag_MallocStackLogging_enableDuringAttach" = 0;
    "param_diag_MallocStackLogging_enableForXPC" = 1;
    "param_diag_allowLocationSimulation" = 1;
    "param_diag_checker_tpc_enable" = 1;
    "param_diag_gpu_frameCapture_enable" = 3;
    "param_diag_gpu_shaderValidation_enable" = 0;
    "param_diag_gpu_validation_enable" = 0;
    "param_diag_memoryGraphOnResourceException" = 0;
    "param_diag_queueDebugging_enable" = 0;
    "param_diag_runtimeProfile_generate" = 0;
    "param_diag_sanitizer_asan_enable" = 0;
    "param_diag_sanitizer_tsan_enable" = 0;
    "param_diag_sanitizer_tsan_stopOnIssue" = 0;
    "param_diag_sanitizer_ubsan_stopOnIssue" = 0;
    "param_diag_showNonLocalizedStrings" = 0;
    "param_diag_viewDebugging_enabled" = 1;
    "param_diag_viewDebugging_insertDylibOnLaunch" = 1;
    "param_install_style" = 0;
    "param_launcher_UID" = 2;
    "param_launcher_allowDeviceSensorReplayData" = 0;
    "param_launcher_kind" = 0;
    "param_launcher_style" = 0;
    "param_launcher_substyle" = 0;
    "param_runnable_appExtensionHostRunMode" = 0;
    "param_runnable_productType" = "com.apple.product-type.application";
    "param_testing_launchedForTesting" = 0;
    "param_testing_suppressSimulatorApp" = 0;
    "param_testing_usingCLI" = 0;
    "sdk_canonicalName" = "iphoneos17.0";
    "sdk_osVersion" = "17.0";
    "sdk_variant" = iphoneos;
}
--


System Information

macOS Version 13.4 (Build 22F66)
Xcode 15.0 (22181.17) (Build 15A5160n)
Timestamp: 2023-06-17T18:19:16+08:00
```

Use Xcode 15 build on iOS 17 error log;
```
Thread 1 Queue : com.apple.main-thread (serial)
#0    0x00000074a9bd57f6 in 0x74a9bd57f6 ()
#1    0x0000000110cdb920 in burst.initialize.statics3 ()
#2    0x0000000110d13340 in Staticburst_initialize ()
#3    0x000000010ff327fc in ::burst_initialize(void *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Libraries/lib_burst_generated.cpp:8
#4    0x000000010ffcef44 in ::StaticResolve() at /Users/bokken/buildslave/unity/build/Runtime/Burst/Burst.cpp:1067
#5    0x000000010ffce3f8 in ::CompileAsync() at /Users/bokken/buildslave/unity/build/Runtime/Burst/Burst.cpp:334
#6    0x000000010ffcf570 in ::CompileAsyncDelegateMethod() at /Users/bokken/buildslave/unity/build/Runtime/Burst/BurstDelegateCache.cpp:45
#7    0x000000010ff34b48 in ::BurstCompilerService_CUSTOM_CompileAsyncDelegateMethod() at /Users/bokken/buildslave/unity/build/artifacts/iOS/Modules/iOS_arm64_nondev_i_r/Bindings/CoreBindings.gen.cpp:11211
#8    0x0000000113d022b4 in ::BurstCompilerService_CompileAsyncDelegateMethod_mDEA0EF934BF3674C1B47014A7518886D1DC2FE80(RuntimeObject *, String_t *, const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/UnityEngine.CoreModule.cpp:9991
#9    0x0000000112aedfc4 in ::BurstCompilerHelper_IsCompiledByBurst_m0239AE7BCAF7076EE75C46D528F04AC34F3761DD(Delegate_t *, const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Unity.Burst.cpp:7462
#10    0x0000000112aee108 in ::BurstCompilerHelper__cctor_m2B57C7C8A7B5F4CEE1E1DE05C5FC63C10AE37FD3(const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Unity.Burst.cpp:7490
#11    0x000000010faab134 in RuntimeInvoker_FalseVoid_t4861ACF8F4594C3437BB48B6E56783494B843915(void (*)(), MethodInfo const*, void*, void**, void*) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Il2CppInvokerTable.cpp:156544
#12    0x0000000110c8186c in il2cpp::vm::Runtime::InvokeWithThrow(MethodInfo const*, void*, void**) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:576
#13    0x0000000110c816b4 in il2cpp::vm::Runtime::Invoke(MethodInfo const*, void*, void**, Il2CppException**) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:562
#14    0x0000000110c7fbf0 in il2cpp::vm::Runtime::ClassInit(Il2CppClass*) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:917
#15    0x000000010f4ef484 in il2cpp_codegen_runtime_class_init_inline(Il2CppClass*) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Libraries/libil2cpp/include/codegen/il2cpp-codegen-il2cpp.h:657
#16    0x0000000112aec790 in ::BurstCompiler_Compile_m0038D8F2B6CB3915CB12F71E15B14C7355BFC8EF(RuntimeObject *, MethodInfo_t *, bool, bool, const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Unity.Burst.cpp:6672
#17    0x0000000112aec064 in ::BurstCompiler_CompileILPPMethod2_m545A8FC57B460871C1715F32DD601F2C1CA9C7FA(RuntimeMethodHandle_tB35B96E97214DCBE20B0B02B1E687884B34680B2, const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Unity.Burst.cpp:6298
#18    0x0000000112b98018 in ::Try_00000A42U24BurstDirectCall_Constructor_mB110B90A1753DDA76BEC765734BA51044BCA4EF3(const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Unity.Collections.cpp:11701
#19    0x0000000112b98078 in ::Try_00000A42U24BurstDirectCall__cctor_m3C84AC61BB336450883D955E604F084A18F335EE(const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Unity.Collections.cpp:11718
#20    0x000000010faab134 in RuntimeInvoker_FalseVoid_t4861ACF8F4594C3437BB48B6E56783494B843915(void (*)(), MethodInfo const*, void*, void**, void*) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Il2CppInvokerTable.cpp:156544
#21    0x0000000110c8186c in il2cpp::vm::Runtime::InvokeWithThrow(MethodInfo const*, void*, void**) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:576
#22    0x0000000110c816b4 in il2cpp::vm::Runtime::Invoke(MethodInfo const*, void*, void**, Il2CppException**) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:562
#23    0x0000000110c7fbf0 in il2cpp::vm::Runtime::ClassInit(Il2CppClass*) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:917
#24    0x000000010f4ef484 in il2cpp_codegen_runtime_class_init_inline(Il2CppClass*) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Libraries/libil2cpp/include/codegen/il2cpp-codegen-il2cpp.h:657
#25    0x0000000112bf2974 in ::U24BurstDirectCallInitializer_Initialize_mBB7299DE1F1DF732C60394307234ED45AE14AD82(const RuntimeMethod *) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Unity.Collections2.cpp:1726
#26    0x000000010faab134 in RuntimeInvoker_FalseVoid_t4861ACF8F4594C3437BB48B6E56783494B843915(void (*)(), MethodInfo const*, void*, void**, void*) at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/Native/Il2CppInvokerTable.cpp:156544
#27    0x0000000110c8186c in il2cpp::vm::Runtime::InvokeWithThrow(MethodInfo const*, void*, void**) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:576
#28    0x0000000110c816b4 in il2cpp::vm::Runtime::Invoke(MethodInfo const*, void*, void**, Il2CppException**) at /Users/bokken/buildslave/unity/build/External/il2cpp/builds/libil2cpp/vm/Runtime.cpp:562
#29    0x000000011017f72c in ::scripting_method_invoke() at /Users/bokken/buildslave/unity/build/Runtime/ScriptingBackend/Il2Cpp/ScriptingApi_Il2Cpp.cpp:292
#30    0x000000011018b160 in ::Invoke() at /Users/bokken/buildslave/unity/build/Runtime/Scripting/ScriptingInvocation.cpp:298
#31    0x0000000110096330 in Invoke [inlined] at /Users/bokken/buildslave/unity/build/Runtime/Scripting/ScriptingInvocation.h:71
#32    0x000000011009631c in ::Execute() at /Users/bokken/buildslave/unity/build/Runtime/Misc/RuntimeInitializeOnLoadManager.cpp:253
#33    0x0000000110096250 in ::ExecuteInitializeOnLoad() at /Users/bokken/buildslave/unity/build/Runtime/Misc/RuntimeInitializeOnLoadManager.cpp:238
#34    0x000000010fff7a74 in Invoke [inlined] at /Users/bokken/buildslave/unity/build/Runtime/Core/Callbacks/CallbackArray.h:70
#35    0x000000010fff7a5c in ::Invoke() at /Users/bokken/buildslave/unity/build/Runtime/Core/Callbacks/CallbackArray.h:331
#36    0x00000001100a1c90 in ::PlayerInitEngineGraphics() at /Users/bokken/buildslave/unity/build/Runtime/Misc/Player.cpp:523
#37    0x00000001106f30a0 in UnityInitApplicationGraphics at /Users/bokken/buildslave/unity/build/PlatformDependent/iPhonePlayer/LibEntryPoint.mm:198
#38    0x000000010f4d5228 in -[UnityAppController startUnity:] at /Users/edmund/Desktop/Github/Oxford_XR_IS_Content/iosBuild/Classes/UnityAppController.mm:121
#39    0x00000001a5240c44 in __NSFireDelayedPerform ()
#40    0x00000001a627399c in __CFRUNLOOP_IS_CALLING_OUT_TO_A_TIMER_CALLBACK_FUNCTION__ ()
#41    0x00000001a6233d2c in __CFRunLoopDoTimer ()
#42    0x00000001a61dd724 in __CFRunLoopDoTimers ()
#43    0x00000001a6226518 in __CFRunLoopRun ()
#44    0x00000001a622adb0 in CFRunLoopRunSpecific ()
#45    0x00000001e7bc5224 in GSEventRunModal ()
#46    0x00000001a868c64c in -[UIApplication _run] ()
#47    0x00000001a868c2b0 in UIApplicationMain ()
#48    0x0000000104d48610 in main at /Users/edmund/Desktop/Github/Education_ARVR/ios/MainApp/AppDelegate.swift:5
#49    0x00000001c8bc74f8 in start ()
Thread 2Thread 4Thread 5com.apple.uikit.eventfetch-thread (7)Thread 9com.apple.SwiftUI.AsyncRenderer (10)AssetGarbageCollectorHelper (11)AssetGarbageCollectorHelper (12)AssetGarbageCollectorHelper (13)AssetGarbageCollectorHelper (14)AssetGarbageCollectorHelper (15)GC Finalizer (16)Job.Worker 0 (17)Job.Worker 1 (18)Job.Worker 2 (19)Job.Worker 3 (20)Job.Worker 4 (21)Background Job.Worker 0 (22)Background Job.Worker 1 (23)Background Job.Worker 2 (24)Background Job.Worker 3 (25)Background Job.Worker 4 (26)Background Job.Worker 5 (27)Background Job.Worker 6 (28)Background Job.Worker 7 (29)Background Job.Worker 8 (30)Background Job.Worker 9 (31)Background Job.Worker 10 (32)Background Job.Worker 11 (33)Background Job.Worker 12 (34)Background Job.Worker 13 (35)Background Job.Worker 14 (36)Background Job.Worker 15 (37)BatchDeleteObjects (38)Loading.AsyncRead (39)caulk::deferred_logger (40)caulk.messenger.shared:high (41)Thread 42AURemoteIO::IOThread (43)Thread 44

```
