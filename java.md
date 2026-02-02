### [java oops](https://www.geeksforgeeks.org/java/object-oriented-programming-oops-concept-in-java/)
What is I/O Buffering?

I/O buffering is a technique where data is temporarily stored in a memory area called a buffer during input/output operations.

📌 Why needed?
Because:

CPU is very fast

I/O devices (disk, keyboard, printer, network) are slow

Buffering allows both to work independently, without waiting for each other.

🔹 Definition (Simple)

I/O buffering temporarily stores data in main memory to handle speed mismatch between the producer (I/O device) and consumer (CPU/process), improving system performance.

🔹 Uses of I/O Buffering
1️⃣ Handle Speed Mismatch

Producer (e.g., modem) produces data faster

Consumer (e.g., disk) consumes data slower

Buffer stores data until it can be processed

2️⃣ Reduce I/O Operations

Instead of writing byte by byte, data is written in blocks

Fewer system calls → better performance

3️⃣ Overlap I/O and Processing

While one buffer is being processed,

Another buffer can receive new data

4️⃣ Support Different Data Sizes

Devices may send data in different formats and sizes

Buffer smooths these variations

🔹 Example (Modem → Memory → Disk)

Modem receives data and fills Buffer 1

Buffer 1 is written to disk

Meanwhile, modem fills Buffer 2

This continues alternately

➡️ This avoids idle time for both modem and disk.

🔹 Types of I/O Buffering Techniques
1️⃣ Single Buffering
🔸 Concept

Only one buffer is used between device and process

🔸 Working

Device writes data into buffer

Process reads data from buffer

Device must wait until buffer is free again

🔸 Device Types
✅ Block-Oriented Devices (Disk)

Data transferred in blocks

While process handles one block, OS may read the next block

Some overlap is possible

✅ Stream-Oriented Devices (Keyboard, Terminal)

Line-at-a-time: Input ends at Enter key

Byte-at-a-time: Every keystroke is processed

🔸 Advantages

✔ Simple to implement
✔ Requires less memory

🔸 Disadvantages

❌ Device or process may remain idle
❌ Limited performance improvement

2️⃣ Double Buffering
🔸 Concept

Uses two buffers

Also called buffer swapping

🔸 Working

Buffer 1 → filled by device

Buffer 2 → processed by user

Then roles are swapped

➡️ Continuous data flow

🔸 Device Types
✅ Block-Oriented

One buffer used by device

Other buffer used by user process

Better CPU–I/O overlap

✅ Stream-Oriented

Line-at-a-time: Process usually doesn’t wait

Byte-at-a-time: No major advantage over single large buffer

🔸 Advantages

✔ Better CPU utilization
✔ Reduces waiting time

🔸 Disadvantages

❌ More complex
❌ Extra memory required
❌ Inefficient for very fast I/O bursts

3️⃣ Circular Buffering
🔸 Concept

Uses more than two buffers

Buffers arranged in a circular queue

🔸 Working

Producer writes to next free buffer

Consumer reads from next full buffer

Pointers move circularly

⚠️ Producer cannot overwrite unread data

🔸 Where Used?

Audio streaming

Video playback

Network packets

Real-time systems

🔸 Advantages

✔ Excellent for continuous data streams
✔ Minimizes data loss
✔ High throughput

🔸 Disadvantages

❌ More complex logic
❌ Needs careful synchronization
