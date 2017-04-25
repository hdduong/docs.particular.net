**Versions 6 and above:** The value recorded in the TimeSent header is the time when the call to send the message is executed, not the actual time when the message was dispatched to the transport infrastructure. Since the outgoing messages in handlers are sent in [batches](/nservicebus/messaging/batched-dispatch.md), the actual dispatch may happen later than the time recorded in the TimeSent header. For operations outside of handlers the recorded sent time is accurate.