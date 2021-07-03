# telnet-codec
A bone-simple Telnet "codec" for use with Rust's Tokio-utils, written by The Mudcano Project.

Create a TelnetCodec, use it to wrap up your TcpStream or TlsStream, and have fun.

Note: The only way to implement MCCP2/3 using this Codec would be to wrap up the TcpStream/TlsStream in one that will
handle the compression, and then stick THAT into this. You'd then be able to toggle compression on the wrapped stream
on and off.