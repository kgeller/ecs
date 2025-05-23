---
mapped_pages:
  - https://www.elastic.co/guide/en/ecs/current/ecs-dll.html
applies_to:
  stack: all
  serverless: all
---
% This file is automatically generated. Don't edit it manually!

# DLL fields [ecs-dll]

These fields contain information about code libraries dynamically loaded into processes.



Many operating systems refer to "shared code libraries" with different names, but this field set refers to all of the following:

* Dynamic-link library (`.dll`) commonly used on Windows

* Shared Object (`.so`) commonly used on Unix-like operating systems

* Dynamic library (`.dylib`) commonly used on macOS

## DLL field details [_dll_field_details]

| Field | Description | Level |
| --- | --- | --- |
| $$$field-dll-name$$$ [dll.name](#field-dll-name) | Name of the library.<br><br>This generally maps to the name of the file on disk.<br><br>type: keyword<br><br>example: `kernel32.dll` | core |
| $$$field-dll-origin-referrer-url$$$ [dll.origin_referrer_url](#field-dll-origin-referrer-url) | _This field is beta and subject to change._ The URL of the webpage that linked to the dll file.<br><br>type: keyword<br><br>example: `http://example.com/article1.html` | extended |
| $$$field-dll-origin-url$$$ [dll.origin_url](#field-dll-origin-url) | _This field is beta and subject to change._ The URL where the dll file is hosted.<br><br>type: keyword<br><br>example: `http://example.com/files/example.dll` | extended |
| $$$field-dll-path$$$ [dll.path](#field-dll-path) | Full file path of the library.<br><br>type: keyword<br><br>example: `C:\Windows\System32\kernel32.dll` | extended |


### Field sets that can be nested under DLL [ecs-dll-nestings]

| Location | Field Set | Description |
| --- | --- | --- |
| `dll.code_signature.*` | [code_signature](/reference/ecs-code_signature.md) | These fields contain information about binary code signatures. |
| `dll.hash.*` | [hash](/reference/ecs-hash.md) | Hashes, usually file hashes. |
| `dll.pe.*` | [pe](/reference/ecs-pe.md) | These fields contain Windows Portable Executable (PE) metadata. |
