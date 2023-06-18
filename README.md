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

[UnityMemory] Configuration Parameters - Can be set up in boot.config
    "memorysetup-bucket-allocator-granularity=16"
    "memorysetup-bucket-allocator-bucket-count=8"
    "memorysetup-bucket-allocator-block-size=4194304"
    "memorysetup-bucket-allocator-block-count=1"
    "memorysetup-main-allocator-block-size=16777216"
    "memorysetup-thread-allocator-block-size=16777216"
    "memorysetup-gfx-main-allocator-block-size=16777216"
    "memorysetup-gfx-thread-allocator-block-size=16777216"
    "memorysetup-cache-allocator-block-size=4194304"
    "memorysetup-typetree-allocator-block-size=2097152"
    "memorysetup-profiler-bucket-allocator-granularity=16"
    "memorysetup-profiler-bucket-allocator-bucket-count=8"
    "memorysetup-profiler-bucket-allocator-block-size=4194304"
    "memorysetup-profiler-bucket-allocator-block-count=1"
    "memorysetup-profiler-allocator-block-size=16777216"
    "memorysetup-profiler-editor-allocator-block-size=1048576"
Built from '2021.3/staging' branch, Version '2021.3.21f1 (1b156197d683)', Build type 'Release', Scripting Backend 'il2cpp'
    "memorysetup-temp-allocator-size-main=4194304"
    "memorysetup-job-temp-allocator-block-size=2097152"
    "memorysetup-job-temp-allocator-block-size-background=1048576"
    "memorysetup-job-temp-allocator-reduction-small-platforms=262144"
    "memorysetup-temp-allocator-size-background-worker=32768"
    "memorysetup-temp-allocator-size-job-worker=262144"
    "memorysetup-temp-allocator-size-preload-manager=262144"
    "memorysetup-temp-allocator-size-nav-mesh-worker=65536"
    "memorysetup-temp-allocator-size-audio-worker=65536"
    "memorysetup-temp-allocator-size-cloud-worker=32768"
    "memorysetup-temp-allocator-size-gfx=262144"
MemoryManager: Using 'Default' Allocator.
Thread Performance Checker: Thread running at QOS_CLASS_USER_INTERACTIVE waiting on a thread without a QoS class specified. Investigate ways to avoid priority inversions
PID: 6159, TID: 364516
Backtrace
=================================================================
3   UnityFramework                      0x0000000107453c98 _ZN12UnityClassic31Baselib_SystemSemaphore_AcquireENS_30Baselib_SystemSemaphore_HandleE + 28
4   UnityFramework                      0x0000000106d9b2c0 _ZN9AGCThreadC2Ev + 204
5   UnityFramework                      0x0000000106d94fb8 _ZN13AGCThreadPoolC2Ev + 148
6   UnityFramework                      0x0000000106d9bdc0 _ZN29AssetGarbageCollectorInstanceC2Ev + 24
7   UnityFramework                      0x0000000106e13604 _ZN17RuntimeStaticBase14InitializeImplEmPFPvS0_10MemLabelIdE + 88
8   UnityFramework                      0x0000000106e0fe70 _ZN35RegisterRuntimeInitializeAndCleanup22ExecuteInitializationsEv + 220
9   UnityFramework                      0x0000000106d97424 _Z17RuntimeInitializev + 80
10  UnityFramework                      0x00000001072e3d08 UnityInitRuntime + 264
11  UnityFramework                      0x0000000106aeb970 -[UnityFramework frameworkWarmup:argv:] + 36
12  UnityFramework                      0x0000000106aeb9b8 -[UnityFramework runUIApplicationMainWithArgc:argv:] + 40
13  Myproject                           0x000000010248012c main + 60
14  dyld                                0x00000001c8bc74f8 F480DCAC-5BC2-3AB7-A817-CAD4CB120667 + 87288

-> applicationDidFinishLaunching()
-> applicationDidBecomeActive()

[Subsystems] Discovering subsystems at path /private/var/containers/Bundle/Application/DB0286A6-D3AD-4600-A9A2-3399B0B7BD71/Myproject.app/Data/UnitySubsystems
GfxDevice: creating device client; threaded=1; jobified=0
Initializing Metal device caps: Apple A15 GPU
Initialize engine version: 2021.3.21f1 (1b156197d683)
Thread Performance Checker: Thread running at QOS_CLASS_USER_INTERACTIVE waiting on a thread without a QoS class specified. Investigate ways to avoid priority inversions
PID: 6159, TID: 364516
Backtrace
=================================================================
3   UnityFramework                      0x0000000107453c98 _ZN12UnityClassic31Baselib_SystemSemaphore_AcquireENS_30Baselib_SystemSemaphore_HandleE + 28
4   UnityFramework                      0x0000000106f14ce4 _ZN15GfxDeviceClient22AcquireThreadOwnershipEv + 172
5   UnityFramework                      0x0000000106f08d6c _Z21CreateClientGfxDevice17GfxDeviceRenderer20GfxCreateDeviceFlags + 252
6   UnityFramework                      0x00000001071d7a2c _Z15CreateGfxDevice17GfxDeviceRenderer20GfxCreateDeviceFlags + 264
7   UnityFramework                      0x00000001071d7ac4 _Z19InitializeGfxDevicev + 112
8   UnityFramework                      0x00000001072e3ec0 UnityInitApplicationGraphics + 20
9   UnityFramework                      0x0000000106ae6fc4 -[UnityAppController startUnity:] + 52
10  Foundation                          0x00000001a5240c44 __NSFireDelayedPerform + 372
11  CoreFoundation                      0x00000001a627399c 5580A260-85DE-375D-933E-4E6035C60CC1 + 825756
12  CoreFoundation                      0x00000001a6233d2c 5580A260-85DE-375D-933E-4E6035C60CC1 + 564524
13  CoreFoundation                      0x00000001a61dd724 5580A260-85DE-375D-933E-4E6035C60CC1 + 210724
14  CoreFoundation                      0x00000001a6226518 5580A260-85DE-375D-933E-4E6035C60CC1 + 509208
15  CoreFoundation                      0x00000001a622adb0 CFRunLoopRunSpecific + 600
16  GraphicsServices                    0x00000001e7bc5224 GSEventRunModal + 164
17  UIKitCore                           0x00000001a868c64c 72A228BE-E5ED-3515-A3EA-53DE3D120375 + 3741260
18  UIKitCore                           0x00000001a868c2b0 UIApplicationMain + 340
19  UnityFramework                      0x0000000106aeb9ec -[UnityFramework runUIApplicationMainWithArgc:argv:] + 92
20  Myproject                           0x000000010248012c main + 60
21  dyld                                0x00000001c8bc74f8 F480DCAC-5BC2-3AB7-A817-CAD4CB120667 + 87288
Thread Performance Checker: Thread running at QOS_CLASS_USER_INTERACTIVE waiting on a thread without a QoS class specified. Investigate ways to avoid priority inversions
PID: 6159, TID: 364516
Backtrace
=================================================================
3   UnityFramework                      0x0000000107453c98 _ZN12UnityClassic31Baselib_SystemSemaphore_AcquireENS_30Baselib_SystemSemaphore_HandleE + 28
4   UnityFramework                      0x0000000106d4aebc _ZN7Texture33VerifyFileTextureUploadCompletionEv + 1024
5   UnityFramework                      0x0000000106d04db8 _ZN9Texture2D33VerifyFileTextureUploadCompletionEv + 80
6   UnityFramework                      0x0000000106d04e60 _ZN9Texture2D13AwakeFromLoadE17AwakeFromLoadMode + 32
7   UnityFramework                      0x0000000106ec27dc _ZN18AwakeFromLoadQueue28InvokePersistentManagerAwakeEPNS_4ItemEj17AwakeFromLoadModeb + 332
8   UnityFramework                      0x0000000106ec25e0 _ZN18AwakeFromLoadQueue30PersistentManagerAwakeFromLoadEi17AwakeFromLoadModeb + 148
9   UnityFramework                      0x0000000106ec4a04 _ZN17PersistentManager27IntegrateAllThreadedObjectsEv + 136
10  UnityFramework                      0x0000000106ec6d28 _ZN17PersistentManager18LoadFileCompletelyEN4core16basic_string_refIcEE + 120
11  UnityFramework                      0x0000000106cc6954 _Z24PlayerLoadGlobalManagersPKcS0_j + 504
12  UnityFramework                      0x0000000106d96f14 _Z24PlayerInitEngineGraphicsb + 180
13  UnityFramework                      0x00000001072e3ee8 UnityInitApplicationGraphics + 60
14  UnityFramework                      0x0000000106ae6fc4 -[UnityAppController startUnity:] + 52
15  Foundation                          0x00000001a5240c44 __NSFireDelayedPerform + 372
16  CoreFoundation                      0x00000001a627399c 5580A260-85DE-375D-933E-4E6035C60CC1 + 825756
17  CoreFoundation                      0x00000001a6233d2c 5580A260-85DE-375D-933E-4E6035C60CC1 + 564524
18  CoreFoundation                      0x00000001a61dd724 5580A260-85DE-375D-933E-4E6035C60CC1 + 210724
19  CoreFoundation                      0x00000001a6226518 5580A260-85DE-375D-933E-4E6035C60CC1 + 509208
20  CoreFoundation                      0x00000001a622adb0 CFRunLoopRunSpecific + 600
21  GraphicsServices                    0x00000001e7bc5224 GSEventRunModal + 164
22  UIKitCore                           0x00000001a868c64c 72A228BE-E5ED-3515-A3EA-53DE3D120375 + 3741260
23  UIKitCore                           0x00000001a868c2b0 UIApplicationMain + 340
24  UnityFramework                      0x0000000106aeb9ec -[UnityFramework runUIApplicationMainWithArgc:argv:] + 92
25  Myproject                           0x000000010248012c main + 60
26  dyld                                0x00000001c8bc74f8 F480DCAC-5BC2-3AB7-A817-CAD4CB120667 + 87288
