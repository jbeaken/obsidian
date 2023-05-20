new binary framing mechanism

-   _Stream_: A bidirectional flow of bytes within an established connection, which may carry one or more messages.
-   _Message_: A complete sequence of frames that map to a logical request or response message.
-   _Frame_: The smallest unit of communication in HTTP/2, each containing a frame header, which at a minimum identifies the stream to which the frame belongs.
- 
The relation of these terms can be summarized as follows:

-   All communication is performed over a single TCP connection that can carry any number of bidirectional streams.
-   Each stream has a unique identifier and optional priority information that is used to carry bidirectional messages.
-   Each message is a logical HTTP message, such as a request, or response, which consists of one or more frames.
-   The frame is the smallest unit of communication that carries a specific type of data—e.g., HTTP headers, message payload, and so on. Frames from different streams may be interleaved and then reassembled via the embedded stream identifier in the header of each frame.