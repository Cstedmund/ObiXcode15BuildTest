# ObiXcode15BuildTest
ObiXcode15BuildTest


Obi got a runtime error on ios devices when the app is Compile and build on xcode 15.
Product work fine under the same system setting when using xcode 14.3

ystem：MacOS 13.4
Devices M1 chip Macbook
Unity Version: 2021.3.11 & 2021.3.21
Obi Version : lastest

Use Xcode 15 build on iOS 17 will break on void burst_initialize(void* i) { Staticburst_initialize(i); }.

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
