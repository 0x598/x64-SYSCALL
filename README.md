x64 syscall caller in C++.

<Usage examples (indexes from Windows 10, build 1803):

**ObjectAttributes.Length = sizeof( OBJECT_ATTRIBUTES );
ClientId.UniqueProcess	= HANDLE( 1000 ); // PID

// NtOpenProcess
Syscall( 0x26, &Handle, PROCESS_TERMINATE, &ObjectAttributes, &ClientId );

// NtTerminateProcess
Syscall( 0x2C, Handle );**>

