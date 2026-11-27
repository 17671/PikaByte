  > **Chapter 2: Hardware & Von Neumann Model**

# Stage 1: Von Neumann Model

## Learning Goals

By the end of this stage, you will be able to:

1. Identify core physical components of computers and explain basic functions.
2. Describe the von Neumann model and why it matters.
3. Explain the fetch-decode-execute process.
4. Describe the CPU and its two parts, the control unit and the ALU.
5. Explain the roles of memory, input, and output.

**Topics covered:**

- Definition
- Process (fetch-decode-execute)
- Components (1): CPU (control unit and ALU)
- Components (2): Memory, Input, and Output

---

# 1.1 Definition

## Explanation

Early computers had a big problem. Every time they needed to do a new job, people had to **rewire** them by hand. This took a long time.

Around 1944–1945, a mathematician named **John von Neumann** came up with a better idea. He noticed that **programs and data are really the same kind of thing: information**. (A **program** is a list of instructions that tells the computer what to do, and **data** is the information the program works on.) So, he suggested that a program should be **stored in the computer's memory**, right next to the data it uses.

This idea created the **von Neumann model**, which is the base of **most modern computers**.

The model divides a computer into **four subsystems**. A **subsystem** is a smaller part that does one main job within the whole computer.

| Subsystem | Its job |
|-----------|---------|
| **Memory** | Stores both programs and data |
| **Arithmetic Logic Unit (ALU)** | Performs calculations and logic operations |
| **Control Unit** | Manages all the operations |
| **Input/Output** | Handles the exchange of data with the outside world |

The big benefit: because the program and data sit in the **same memory**, a computer can **switch easily between tasks**, without anyone needing to rewire the machine.

## Worked Example

**Task:** Explain how a computer changes from playing music to editing a document.

| Old way (before von Neumann) | Von Neumann way |
|------------------------------|-----------------|
| Engineers rewire the machine for the new job | The new program is loaded into memory |
| Slow and difficult | Fast and easy |

In the von Neumann model, the computer simply loads the document-editing program into memory, and the control unit starts following its instructions.

## Activity

a. What big idea did von Neumann add to computer design?
b. Name the four subsystems of the von Neumann model.
c. Why does storing programs in memory make switching tasks easier?

<details>
<summary><b>Answer</b></summary>

a. Programs should be **stored in the computer's memory**, together with the data.
b. **Memory, Arithmetic Logic Unit (ALU), Control Unit, and Input/Output.**
c. To change tasks, the computer just loads a different program into memory. No one has to **rewire** the machine.

</details>

---

# 1.2 Process: Fetch-Decode-Execute

## Explanation

In the von Neumann model, the computer follows its program **one instruction at a time, in order**. This keeps programs running in an organized and predictable way. (An **instruction** is a single step the computer can carry out, such as "add these two numbers".)

For each instruction, the computer repeats a three-step cycle called the **fetch-decode-execute cycle**:

| Step | What happens | Who does it |
|------|--------------|-------------|
| **1. Fetch** | The next instruction is **fetched** (brought) from memory | Control unit |
| **2. Decode** | The instruction is **decoded**, which means its meaning is worked out and the right parts are told what to do | Control unit |
| **3. Execute** | The instruction is **executed** (carried out) | ALU, or another part such as input/output |

After the execute step, the computer moves on to the **next instruction** and the cycle starts again. The computer remembers where it is in the program using a small storage spot called the **program counter**. The program counter holds the **address** (the location number in memory) of the next instruction.

## Worked Example

**Task:** A program in memory has two instructions:

1. Add 4 and 6, and store the result.
2. Output the result.

| Cycle | Step | What happens |
|-------|------|--------------|
| 1 | Fetch | The control unit gets "Add 4 and 6" from memory |
| 1 | Decode | The control unit works out that this means "add" and tells the ALU |
| 1 | Execute | The ALU calculates 4 + 6 = 10, and the result is stored in memory |
| 2 | Fetch | The program counter moves on, and the control unit gets "Output the result" |
| 2 | Decode | The control unit works out that this means "send to the screen" |
| 2 | Execute | The output part displays **10** on the screen |

## Activity

a. Put these steps in the correct order: **Execute**, **Fetch**, **Decode**.
b. Which step brings an instruction from memory to the control unit?
c. What does the program counter keep track of?

<details>
<summary><b>Answer</b></summary>

a. **Fetch → Decode → Execute**
b. **Fetch**
c. The **address of the next instruction** to run.

</details>

---

# 1.3 Components (1): The CPU (Control Unit and ALU)

## Explanation

The **Central Processing Unit (CPU)** is the "brain" of the computer. It is the part that **processes** data and carries out instructions. The CPU is made of **two main parts**:

- **Control Unit**
- **Arithmetic Logic Unit (ALU)**

### Control Unit

The **control unit** **manages all the operations** in the computer. You can think of it as a **traffic controller** or a **manager**. It does not do the calculations itself. Instead, it:

- **Fetches** instructions from memory.
- **Decodes** them to understand what they mean.
- **Tells the other parts** (ALU, memory, input/output) what to do and when.

### Arithmetic Logic Unit (ALU)

The **ALU** is the part that does the **actual calculations and comparisons**. It performs two kinds of operations:

| Kind | Meaning | Examples |
|------|---------|----------|
| **Arithmetic operations** | Math on numbers | Add, subtract, multiply, divide |
| **Logic operations** | Comparing values and making true/false decisions | Is 15 greater than 12? Are these two numbers equal? |

So: **CPU = Control Unit + ALU**.

## Worked Example

**Task:** The program says: "If the player's score is more than 100, show 'You win!'" The score is 120.

| Step | Part | What happens |
|------|------|--------------|
| 1 | Control unit | Fetches and decodes the instruction "compare score with 100" |
| 2 | Control unit | Sends the numbers 120 and 100 to the ALU |
| 3 | ALU | Performs a **logic operation**: is 120 > 100? The answer is **True** |
| 4 | Control unit | Sees the answer is True and tells the output part to show "You win!" |

## Activity

Decide whether each job belongs to the **control unit** or the **ALU**:

a. Calculating 25 + 17
b. Deciding which instruction to run next
c. Checking whether two numbers are equal
d. Telling the memory to send an instruction

<details>
<summary><b>Answer</b></summary>

a. **ALU** (arithmetic operation)
b. **Control unit**
c. **ALU** (logic operation)
d. **Control unit**

</details>

---

# 1.4 Components (2): Memory, Input, and Output

## Explanation

The other two subsystems of the von Neumann model are **memory** and **input/output**. Together with the CPU, they make up the computer's **hardware**.

**Hardware** means the **physical components** of a computer, the parts you can touch. The memory, the ALU, and the input/output parts are all hardware.

### Memory

**Memory** is where the computer stores **both programs and data**, in the **same place**. Each location in memory has its own **address**, like a house number, so the control unit can find exactly the instruction or data it needs.

### Input

**Input** is the **data or commands that the computer receives** from users or devices. Examples: typing on a keyboard, moving a mouse, or speaking into a microphone.

### Output

**Output** is the **result that the computer gives back** to the user. Examples: showing text on a screen (a display) or printing a page on a printer.

Together, **input and output let the user and the computer interact** with each other. In the von Neumann model, both are handled by the **Input/Output subsystem**.

| Component | Main job | Example |
|-----------|----------|---------|
| **Memory** | Stores programs and data | The chips that hold your open apps |
| **Input** | Brings data into the computer | Keyboard, mouse, microphone |
| **Output** | Sends results out to the user | Screen, printer, speakers |

## Worked Example

**Task:** You type `5 + 3` into a calculator program and see the answer on the screen. Show how all four subsystems work together.

| Step | Subsystem | What happens |
|------|-----------|--------------|
| 1 | **Input** | You type `5 + 3` on the keyboard, and the computer receives it |
| 2 | **Memory** | The numbers 5 and 3 and the "add" instruction are stored in memory |
| 3 | **Control unit** | Fetches and decodes the "add" instruction |
| 4 | **ALU** | Calculates 5 + 3 = 8 |
| 5 | **Memory** | Stores the result, 8 |
| 6 | **Output** | Displays **8** on the screen |

## Activity

a. What is **hardware**?
b. Which subsystem stores both programs and data?
c. Name one input device and one output device.
d. Put these steps in order for printing a typed letter: **Printer produces the page**, **You type the letter**, **The CPU processes the text**.

<details>
<summary><b>Answer</b></summary>

a. The **physical components** of a computer, such as memory, the ALU, and the input/output parts.
b. **Memory**
c. For example, input device: **keyboard** (or mouse or microphone). Output device: **printer** (or screen or speakers).
d. **You type the letter → The CPU processes the text → The printer produces the page**

</details>

---

## Stage 1 Summary

- The **von Neumann model** says that programs and data are both information, so they can be **stored together in memory**. This lets computers switch tasks easily without being rewired.
- The model has four subsystems: **Memory**, **ALU**, **Control Unit**, and **Input/Output**.
- The computer follows instructions one at a time using the **fetch-decode-execute cycle**: fetch the instruction from memory, decode what it means, and execute it.
- The **CPU** is made of the **control unit** (the manager that directs everything) and the **ALU** (which does arithmetic and logic operations).
- **Memory** stores programs and data. **Input** brings data in, and **output** gives results back to the user.
- **Hardware** is the physical part of a computer.

# Stage 2: Computer Hardware

## Learning Goals

By the end of this stage, you will be able to:

1. Identify core physical components of computers and explain basic functions.
2. Define hardware and tell the difference between internal and external hardware.
3. Describe common input devices: mouse, keyboard, microphone, camera, and touchpad.
4. Describe common output devices: monitor, printer, and speaker.
5. Explain the role of the main internal parts: motherboard, CPU, RAM, ROM, graphics card, and power supply.
6. Describe ports and external storage such as USB drives and memory cards.

**Topics covered:**

- Hardware Definition
- Input Devices: Mouse, Keyboard, Microphone, Camera, Touchpad
- Output Devices: Monitor, Printer, Speaker
- Internal Hardware: Motherboard, CPU, RAM, RAM vs ROM, Graphics Card, Power Supply
- Ports and External Storage: USB, Memory Card

---

# 2.1 Hardware Definition

## Explanation

**Hardware** means the **physical parts of a computer**, the parts you can see and touch. The programs that run on the hardware are called **software**.

Hardware can be split into two groups:

| Group | Meaning | Examples |
|-------|---------|----------|
| **Internal hardware** | Parts **inside** the computer case | Motherboard, CPU, RAM, graphics card, power supply |
| **External hardware** | Parts **outside** the case that connect to the computer. These are also called **peripherals** | Keyboard, mouse, monitor, printer, speakers |

Hardware can also be sorted by its job:

- **Input devices** send data **into** the computer.
- **Output devices** show or deliver results **out of** the computer.
- **Internal hardware** processes, stores, and moves the data.
- **Ports and external storage** connect devices and keep data outside the main case.

## Worked Example

**Task:** Sort each item into **internal** or **external** hardware.

| Item | Group |
|------|-------|
| Keyboard | External |
| CPU | Internal |
| Printer | External |
| RAM | Internal |

## Activity

a. What is hardware?
b. Is a mouse internal or external hardware?
c. Is a word processor program hardware or software?

<details>
<summary><b>Answer</b></summary>

a. The **physical parts** of a computer that you can touch.
b. **External** (it is a peripheral that connects to the computer).
c. **Software** (it is a program, not a physical part).

</details>

---

# 2.2 Input Devices

## Explanation

**Input devices** are the devices used to **give data and commands to the computer**.

| Device | What it does |
|--------|--------------|
| **Keyboard** | One of the most common input devices. Each key matches a **character** (a letter, number, or symbol), a **function**, or a **command**. When you press a key, it creates a **signal** (a small pattern of electricity) that the computer understands as an action, such as typing a letter or running a shortcut. |
| **Mouse** | A **pointing device**: moving it moves a **cursor** (the pointer) on the screen. It lets you **click**, **select**, and **drag** objects in a **graphical user interface (GUI)**, which is a screen with windows, icons, and buttons. Modern mice often have extra buttons and a **scroll wheel**. |
| **Touchpad** | A flat, **touch-sensitive surface**, usually found on laptops. Moving your finger across it moves the cursor, and tapping works like a click. Many touchpads also understand **gestures** (finger movements such as two-finger scrolling). |
| **Camera** | A **visual** input device that **captures images or video** and sends the data to the computer. |
| **Microphone** | Turns **sound waves into electric signals**, so audio can enter the computer. |

**Types of cameras:**

- **Webcam**: A built-in or external camera on a computer, used for video calls.
- **Mobile camera**: Built into a smartphone or tablet. It has a **lens**, a **sensor** (which detects light), and an **image processor**, like a standalone camera but smaller.
- **Digital camera**: Higher quality, often used for photography and video production.

**Types of microphones:**

- **Condenser**: Very sensitive, often used in studios.
- **Dynamic**: Durable, often used for live sound.
- **USB microphone**: **Plug-and-play** (ready to use as soon as you connect it) and good for everyday use.

## Worked Example

**Task:** You join a video call and type a message in the chat. Name the input devices used.

| What you do | Input device |
|-------------|--------------|
| Show your face | Webcam (camera) |
| Speak | Microphone |
| Type the chat message | Keyboard |
| Move the pointer to the "Send" button on a laptop | Touchpad (or mouse) |

## Activity

Name the input device for each job:

a. Recording the sound of a live concert in a tough, durable way.
b. Moving the cursor on a laptop by sliding your finger.
c. Capturing a photo with your phone.
d. Pressing `Ctrl + C` to copy text.

<details>
<summary><b>Answer</b></summary>

a. **Dynamic microphone**
b. **Touchpad**
c. **Mobile camera**
d. **Keyboard**

</details>

---

# 2.3 Output Devices

## Explanation

**Output devices** present the **results of processed data** to the user. After the computer has processed the input, output devices share the results in different forms: **visual** (to see), **auditory** (to hear), or **physical** (to hold).

| Device | What it does |
|--------|--------------|
| **Monitor** | Also called a **display screen**. It shows data as graphics, text, or video. |
| **Printer** | Turns digital data into a **physical form** by printing on paper. |
| **Speaker** | Turns digital data into **sound**. |

### Monitor

Monitors come in several types: **LCD**, **LED**, and **OLED**. They also differ in two measurements:

- **Resolution**: The number of tiny dots (**pixels**) that make up the picture. More pixels give a clearer picture.
- **Refresh rate**: How many times per second the screen **updates** the picture, measured in **hertz (Hz)**. A higher rate makes motion look smoother.

Monitors display the **desktop**, applications, and media, and they give feedback on what the user does. **High-definition** displays are important for graphic design, gaming, and video production, where accurate visuals matter.

### Printer

Printers produce **hard copies** (paper copies) of documents. Common types:

- **Inkjet** and **laser** printers: Used for standard documents and photos.
- **3D printers**: Build **objects layer by layer** from a digital model. They are used in manufacturing, engineering, and medicine.

### Speaker

Speakers **convert digital data into sound**, such as music, videos, alerts, and system notifications. They are important for multimedia and for **accessibility**, because they let visually impaired users get information through sound.

## Worked Example

**Task:** Choose the best output device.

| Need | Device | Why |
|------|--------|-----|
| Watch a movie | Monitor | Shows video |
| Get a paper copy of a school form | Printer (inkjet or laser) | Makes a hard copy |
| Make a physical model of a part from a digital design | 3D printer | Builds objects layer by layer |
| Hear a warning sound from the computer | Speaker | Produces audio |

**Refresh rate example:** A monitor with a refresh rate of 60 Hz updates the picture 60 times every second. A 144 Hz monitor updates it 144 times every second, so motion looks smoother.

## Activity

a. What is a pixel?
b. How many times per second does a 120 Hz monitor update the picture?
c. Which output device helps a visually impaired user hear information from the computer?
d. What is a hard copy?

<details>
<summary><b>Answer</b></summary>

a. One of the **tiny dots** that make up the picture on a screen.
b. **120 times** per second.
c. **Speaker**
d. A **paper copy** of a digital document or image.

</details>

---

# 2.4 Internal Hardware

## Motherboard

### Explanation

The **motherboard** is the **main circuit board** of the computer. It is the **backbone**: it connects all the essential parts and lets them **communicate**, including the CPU, memory, storage, and input/output devices.

The motherboard has several important features:

| Feature | What it does |
|---------|--------------|
| **CPU socket** | The physical spot where the CPU is installed |
| **Memory slots** | Slots where RAM modules are plugged in |
| **Expansion slots** | Slots (such as **PCIe**) for adding extra cards, like a graphics card |
| **Chipset** | A group of chips that controls how the CPU, memory, and other devices work together |
| **Data bus** | The wires that carry data between the parts |
| **Ports** | Connectors for devices (see 2.4) |

### The Data Bus

A **data bus** is a set of wires that moves data between the CPU, memory, and other parts. Its **width**, measured in **bits**, decides how much data can be sent **at the same time**. A wider bus can carry more data in one go. Some important buses are:

| Bus | What it connects |
|-----|------------------|
| **Front-Side Bus (FSB)** | The CPU and main memory (found in older designs) |
| **PCIe (Peripheral Component Interconnect Express)** | High-speed parts such as graphics cards and SSDs |
| **SATA** | The motherboard and storage devices |
| **USB buses** | External devices such as keyboards and drives |

The **bus specs** (specifications, or technical details) decide the **data transfer rate** and the system's performance.

### The Chipset

The **chipset** acts as a controller for the CPU, memory, and other devices. In many computers, it is split into two parts:

- **Northbridge**: Connects the CPU to **high-speed** parts such as RAM and graphics cards.
- **Southbridge**: Manages **lower-speed** parts such as hard drives, USB ports, and expansion slots.

*(In many modern computers, the northbridge's work is built into the CPU itself, and a single chip handles the rest. The idea of fast and slow connections stays the same.)*

[insert image about motherboard architecture: CPU, northbridge, southbridge, memory bus, and PCI bus]

### Worked Example

**Task:** Compare data buses of different widths. How many transfers does it take to send 64 bits?

| Bus width | Bits moved per transfer | Transfers needed for 64 bits |
|-----------|------------------------|-------------------------------|
| 8 bits | 8 | 64 ÷ 8 = **8 transfers** |
| 32 bits | 32 | 64 ÷ 32 = **2 transfers** |
| 64 bits | 64 | 64 ÷ 64 = **1 transfer** |

A wider bus moves the same data in fewer steps.

### Activity

a. What is the motherboard's main job?
b. A 32-bit bus needs to send 128 bits. How many transfers are needed?
c. Which part of the chipset connects the CPU to RAM and graphics cards?

<details>
<summary><b>Answer</b></summary>

a. To **connect all the parts** of the computer and let them communicate.
b. 128 ÷ 32 = **4 transfers**
c. The **northbridge**

</details>

---

## CPU

### Explanation

The **Central Processing Unit (CPU)** is the **"brain"** of the computer. It **executes instructions** and **processes data**. It is installed in the **CPU socket** on the motherboard.

When the computer is switched on, the CPU starts the **boot sequence**. To **boot** means to start up. In the boot sequence, the CPU:

1. **Initializes** (sets up and checks) the hardware parts.
2. **Loads the operating system** (the main software that manages the computer) from storage into memory.

The CPU uses the data bus to **read and write data** to and from RAM and storage devices, which lets it work quickly.

### Worked Example

**Task:** Put the start-up steps of a computer in order.

1. You press the power button.
2. The CPU starts the boot sequence.
3. The hardware parts are initialized.
4. The operating system is loaded from storage into memory.
5. The computer is ready to use.

### Activity

a. Where is the CPU installed?
b. What does "boot" mean?

<details>
<summary><b>Answer</b></summary>

a. In the **CPU socket** on the motherboard.
b. To **start up** the computer, setting up the hardware and loading the operating system.

</details>

---

## RAM and ROM

### Explanation

**RAM (Random Access Memory)** is the computer's fast, **temporary** working memory. When the CPU processes data, it keeps that data in RAM so it can reach it quickly. RAM is plugged into the **memory slots** on the motherboard. How much RAM there is, and how fast it is, affects the system's performance, especially for tasks that need fast access to data.

**ROM (Read Only Memory)** holds data that **cannot be easily changed**. It usually stores **firmware**, which is software built into the hardware to tell it how to start and work. For example, the **BIOS** is firmware that starts up a computer's hardware.

| Feature | RAM | ROM |
|---------|-----|-----|
| Full name | Random Access Memory | Read Only Memory |
| Purpose | Holds data and programs **in use right now** | Holds **start-up instructions** (firmware) |
| Can it be changed easily? | **Yes**, constantly | **No**, not easily |
| When the power goes off | Contents are **lost** (volatile) | Contents are **kept** (non-volatile) |
| Speed | Very fast | Slower than RAM |

### Worked Example

**Task:** Decide whether RAM or ROM is used.

| Situation | Memory | Why |
|-----------|--------|-----|
| A browser with 10 open tabs | RAM | It needs fast, changeable memory |
| The instructions a computer uses to start up | ROM | They must stay when the power is off |
| A game being played | RAM | The CPU needs the data quickly |

### Activity

a. Which memory is lost when the computer is switched off?
b. What is firmware?
c. Which memory is better for holding the start-up instructions, RAM or ROM?

<details>
<summary><b>Answer</b></summary>

a. **RAM**
b. **Software built into hardware** that tells the hardware how to start and work.
c. **ROM**

</details>

---

## Graphics Card

### Explanation

A **graphics card** is an **expansion card** that handles **images and video**. It has its own processor, called a **GPU (Graphics Processing Unit)**, which is built to draw pictures very quickly. It plugs into a **PCIe expansion slot** on the motherboard and sends the picture to the monitor.

A **graphics card** is important for gaming, video editing, and graphic design. Other **expansion cards** work the same way:

- **Sound card**: Improves audio for tasks like professional audio work.
- **Network card**: Connects the computer to a network.

Each expansion card has its own resources and **communicates with the CPU through the motherboard**. This lets users **customize** their computers for the performance they need.

### Worked Example

**Task:** A designer edits 4K video. Which hardware helps most?

| Part | Why it helps |
|------|--------------|
| Graphics card (GPU) | Draws images and video quickly |
| RAM | Holds the video data being edited |
| CPU | Runs the editing program |

### Activity

a. What does GPU stand for?
b. Which slot is a graphics card plugged into?
c. Name another type of expansion card.

<details>
<summary><b>Answer</b></summary>

a. **Graphics Processing Unit**
b. A **PCIe expansion slot** on the motherboard
c. A **sound card** (or **network card**)

</details>

---

## Power Supply

### Explanation

The **power supply unit (PSU)** gives the computer the **electricity** it needs. The electricity from a wall outlet is **AC (alternating current)**, but computer parts need **DC (direct current)** at **lower voltages**. The PSU:

- **Converts** AC from the wall into low-voltage DC.
- **Sends power** through cables to the motherboard, drives, and other parts.

A PSU is rated in **watts (W)**. A more powerful computer, such as one with a strong graphics card, needs a PSU with a higher watt rating.

### Worked Example

**Task:** A computer's parts need about 350 W in total. Which PSU is suitable?

| PSU | Suitable? | Why |
|-----|-----------|-----|
| 250 W | No | Not enough power |
| 500 W | Yes | Covers 350 W with room to spare |

### Activity

a. What does a power supply unit convert?
b. If you add a powerful graphics card, why might you need a bigger PSU?

<details>
<summary><b>Answer</b></summary>

a. **AC** electricity from the wall into low-voltage **DC** for the computer's parts.
b. A powerful graphics card uses **more electricity**, so the PSU must be able to supply more watts.

</details>

---

# 2.5 Ports and External Storage

## Explanation

**Input/output ports** are the **physical connectors** on a computer, such as **USB ports**, **audio jacks**, and **HDMI ports**. They let you connect devices to the computer. There are two types:

| Type | What it connects | Examples |
|------|------------------|----------|
| **Internal port** | The motherboard to devices **inside** the case | Hard disk, CD drive, internal Bluetooth |
| **External port** | The motherboard to devices **outside** the case | Mouse, printer, USB drive |

### USB (Universal Serial Bus)

A **USB port** can connect many kinds of external devices: external hard disks, printers, scanners, mice, keyboards, and more. USB comes in different **shapes** (such as Type A, Type B, and Type C) and different **versions**, which have different **speeds**. Speed is measured in **megabits per second (Mbps)**, where one **megabit** is one million bits.

| USB version | Maximum speed |
|-------------|---------------|
| USB 1.1 (an early version) | 12 Mbps |
| USB 2.0 | 480 Mbps |
| USB 3.0 | 5,000 Mbps (5 Gbps) |

A **USB flash drive** is a small, portable storage device that plugs into a USB port. It is plug-and-play and often used to move files between computers.

### Memory Card

A **memory card** is a small, thin **flash storage** card used to store data in cameras, phones, and other devices. A common type is the **SD card** (Secure Digital card), and a smaller version is the **microSD card**. You can read a memory card by putting it in a **card slot** or in a **card reader** (a small device that plugs into a USB port).

**External storage** means any storage that is not built permanently inside the computer, such as USB flash drives, external hard drives, and memory cards. It is useful for backups and for carrying files from one device to another.

## Worked Example

**Task:** How long does it take to copy a 600 MB file over each USB version? (A **byte** is 8 bits, so 1 megabyte (MB) = 8 megabits (Mb). These are the best-case speeds. Real speeds are usually a little lower.)

1. Convert the file size: 600 MB × 8 = **4,800 megabits**
2. Time at 12 Mbps (USB 1.1): 4,800 ÷ 12 = **400 seconds** (about 6.7 minutes)
3. Time at 480 Mbps (USB 2.0): 4,800 ÷ 480 = **10 seconds**

A newer USB version moves the same file much faster.

## Activity

a. Name two examples of external ports.
b. How long does it take to copy a 60 MB file at 480 Mbps? (Hint: 60 MB × 8 = 480 megabits.)
c. What device can you use to read an SD card if your computer has no card slot?
d. Give two examples of external storage.

<details>
<summary><b>Answer</b></summary>

a. For example, a **USB port** and an **HDMI port** (or an audio jack).
b. 480 ÷ 480 = **1 second**
c. A **card reader** that plugs into a USB port.
d. For example, a **USB flash drive** and a **memory card** (or an external hard drive).

</details>

---

## Stage 2 Summary

- **Hardware** is the physical part of a computer. **Internal hardware** is inside the case, and **external hardware** (peripherals) connects from outside.
- **Input devices** send data into the computer: **keyboard**, **mouse**, **touchpad**, **camera**, and **microphone**.
- **Output devices** present results: **monitor** (resolution and refresh rate), **printer** (inkjet, laser, 3D), and **speaker**.
- The **motherboard** connects all the parts through the **data bus**, the **chipset**, **memory slots**, **expansion slots**, and **ports**.
- The **CPU** is the brain. It starts the boot sequence and uses the data bus to work with RAM and storage.
- **RAM** is fast, temporary working memory, and **ROM** keeps firmware that starts the hardware.
- A **graphics card (GPU)** handles images and video, and the **power supply** converts wall AC into low-voltage DC for the computer.
- **Ports** connect devices. **USB** connects many kinds of devices, and **memory cards** and USB drives provide portable **external storage**.

# Stage 3: Motherboard Power and BIOS, CPU, and GPU

## Learning Goals

By the end of this stage, you will be able to:

1. Identify core physical components of computers and explain basic functions.
2. Explain how the motherboard shares power and how the BIOS/UEFI starts the computer.
3. Describe the CPU and the fetch-decode-execute cycle.
4. Explain what decides a CPU's speed: clock speed, cache, bus speed, and threads.
5. Describe the GPU, how it works, and why it is useful for graphics, gaming, and AI.

**Topics covered (from Internal Hardware):**

- Motherboard (power distribution and BIOS/UEFI)
- CPU
- Graphics Card (GPU)

---

# 3.1 Internal Hardware

**Hardware** means the physical parts of a computer. **Internal hardware** means the parts that sit **inside** the computer case. The **motherboard** is the main circuit board that connects them all, so it is a good place to start.

---

## Motherboard: Power Distribution and BIOS/UEFI

### Explanation

#### Power distribution

The **power supply unit (PSU)** brings electricity into the computer. The **motherboard** then **shares (distributes) this power** with the other parts, including the **CPU**, **memory**, and **peripheral devices** (devices that connect to the computer, like a mouse or printer).

Each part needs a different amount of power. The motherboard has **voltage regulation circuits**. **Voltage** is the "push" of electricity, measured in **volts**. These circuits make sure **each part receives a steady, correct level of voltage**. This is very important for **reliability** (the computer keeps working without crashing) and for **performance**.

#### BIOS/UEFI

The motherboard also holds a special piece of **firmware**. **Firmware** is software stored permanently inside a hardware device to tell it how to work. This firmware is called:

- **BIOS (Basic Input/Output System)**: The older name.
- **UEFI (Unified Extensible Firmware Interface)**: The newer version that replaces BIOS in most computers.

The BIOS/UEFI has two main jobs:

1. **It starts up the hardware** during the **boot process**. (To **boot** means to start the computer.) It **initializes** the hardware, which means it sets up and checks each part.
2. **It gives you a low-level way to configure the system.** (**Low-level** means close to the hardware, before the normal operating system has even started.) It stores important **settings** for hardware parts, and lets you change the **boot order**, which is the order in which the computer looks for an operating system, and some **hardware performance options**.

### Worked Example

**Task:** A computer has a USB drive plugged in, and you want to start it from the drive instead of the SSD.

| Step | What happens |
|------|--------------|
| 1 | You turn on the computer and open the BIOS/UEFI settings |
| 2 | You change the **boot order** so the USB drive is first and the SSD is second |
| 3 | You save and restart |
| 4 | The BIOS/UEFI initializes the hardware, then looks for an operating system on the USB drive first |

### Activity

a. What does the motherboard do with the electricity it receives from the PSU?
b. Why does the motherboard have voltage regulation circuits?
c. What do BIOS and UEFI stand for?
d. Name two things you can change in the BIOS/UEFI.

<details>
<summary><b>Answer</b></summary>

a. It **distributes** the power to the CPU, memory, and peripheral devices.
b. To make sure **each part gets a stable, correct power level**, which keeps the computer reliable and working well.
c. **Basic Input/Output System** and **Unified Extensible Firmware Interface**.
d. For example: the **boot order**, **hardware settings**, and **performance options**.

</details>

---

## Central Processing Unit (CPU)

### Explanation

The **Central Processing Unit (CPU)** is the **"brain"** of the computer. It **executes instructions** (carries out the steps of programs) and **processes data**. It sits in the **CPU socket** on the motherboard.

When the computer is switched on, the CPU begins the **boot sequence**: it **initializes the hardware** and **loads the operating system** from storage into memory.

Inside the CPU are **millions or even billions of transistors**. A **transistor** is a tiny electronic **switch** that is either on or off. This matches **binary** (the system of `0`s and `1`s), so the CPU receives all its data in binary.

#### The fetch-decode-execute cycle

After the CPU receives input, it follows three steps for every instruction:

| Step | What happens |
|------|--------------|
| **1. Fetch** | The CPU gets the instruction from **RAM**. It uses the **address bus** (a set of wires that carries a memory **address**, which is a location number) to find where the instruction is stored. The instruction is then loaded into the CPU. |
| **2. Decode** | The CPU works out **what the instruction means**, by breaking it into smaller parts it can carry out. |
| **3. Execute** | The CPU carries out the instruction using its **ALU**. The result is stored back in RAM or sent to an **output device**, as needed. |

This cycle repeats in a **continuous loop**, which lets the CPU do complicated tasks quickly.

#### Parts of the CPU

- **Control unit**: Directs how the processor works. It manages the flow of data between the CPU and other parts by **sending signals** that coordinate actions, such as reading from or writing to memory.
- **Arithmetic Logic Unit (ALU)**: The part that does the **actual computing**. It does **arithmetic operations** (add, subtract, multiply, divide) and **logic operations** (comparisons, and the operations AND, OR, and NOT). It takes its inputs from the CPU's **registers**, which are tiny, very fast storage spots inside the CPU, and then outputs the result.
- **Program counter**: A register that holds the **address of the next instruction** to fetch.
- **Instruction register (IR)**: A register that holds the **instruction currently being decoded or executed**.

### Worked Example

**Task 1:** Follow one instruction through the cycle. The instruction "Add 4 and 6" is stored at memory address 100.

| Step | What happens |
|------|--------------|
| Fetch | The program counter points to address 100. The CPU uses the address bus to get the instruction from RAM. |
| Decode | The control unit works out that it means "add". |
| Execute | The ALU calculates 4 + 6 = 10. The result is stored back in RAM. |
| Next | The program counter moves to the next address, and the cycle repeats. |

**Task 2 (clock speed, simplified):** A CPU runs at 3 GHz, and each instruction takes 3 cycles.

1. 3 GHz = 3 billion cycles per second
2. Instructions per second = 3 billion ÷ 3 = **1 billion instructions per second**

### Activity

a. Put these steps in order: **Execute**, **Fetch**, **Decode**.
b. What is the ALU's job?
c. A CPU runs at 4 GHz. How many cycles does it perform each second?
d. Which cache is the fastest: L1, L2, or L3?
e. In the CPU-Z example, how many threads can the Intel Core i5-12500H handle?

<details>
<summary><b>Answer</b></summary>

a. **Fetch → Decode → Execute**
b. To do the **arithmetic** (math) and **logic** (comparison) operations.
c. 4 GHz = **4 billion** cycles per second.
d. **L1**
e. **16 threads**

</details>

---

## Graphics Processing Unit (GPU)

### Explanation

A **Graphics Processing Unit (GPU)** is a **specialized processor** made to handle complex calculations, mainly those used to **draw (render) visuals**, **run games**, and do tasks that need **parallel processing**, such as AI. (**Rendering** means turning data into a finished picture. **Parallel processing** means doing many tasks **at the same time**.)

The GPU works **alongside the CPU**, but it is built to perform **many repetitive calculations at once**. That makes it perfect for graphics-heavy work.

| | CPU | GPU |
|---|-----|-----|
| Style | A few powerful cores that handle varied tasks one after another | Many small cores that handle many simple tasks at the same time |
| Best at | General tasks, running the operating system and programs | Graphics, video, games, and AI calculations |

#### Core components of a GPU

| Component | What it does |
|-----------|--------------|
| **Cores** | Small processing units that run tasks **in parallel**. More cores usually mean better performance for many tasks at once. |
| **Memory (VRAM)** | Video RAM. Stores data needed for drawing, such as **textures** (surface pictures on objects) and **frame buffers**. It lets the GPU work fast without always using the system's RAM. |
| **Memory interface** | Controls the flow of data between the VRAM and the GPU cores. It affects how fast the GPU can reach stored data. Common memory types are **GDDR** (Graphics Double Data Rate), such as **GDDR6** or **GDDR6X**, built for high-speed transfers. |
| **Shaders** | Specialized units that handle **lighting, color**, and other visual effects. |
| **Rasterizer** | Turns **3D objects into pixels** to show on a flat, 2D screen. (A **pixel** is one tiny dot of a picture.) |
| **Frame buffer** | Holds the **finished image** before it is sent to the display. |
| **Control logic** | Directs the cores and **schedules** (organizes) their tasks. |

#### How a GPU works

1. **Input data**: The CPU sends the GPU data, such as textures, **vertices** (corner points of 3D shapes), and shaders.
2. **Parallel processing**: The GPU's many cores split the data into small tasks and work on them **at the same time**.
3. **Rendering**: The tasks include calculating images, textures, and animations.
4. **Output**: The finished data is sent to the **display**, producing images or video.

#### What GPUs are used for

- **Complex visuals and rendering**: GPUs draw 2D and 3D graphics, animations, and video. In video editing, **CAD** (Computer-Aided Design, used to design objects), and animation, the GPU handles shading, textures, and polygon creation much faster than a CPU.
- **Gaming**: Modern games need **high frame rates** (many images per second), realistic lighting, shadows, and physics. GPUs make smooth, lifelike visuals possible, including in **virtual reality (VR)**.
- **Artificial intelligence and machine learning**: AI training uses a huge number of **matrix multiplications** (repeated multiplying of grids of numbers), which a GPU can do in parallel. Companies such as NVIDIA build specialized GPUs for AI.

#### Integrated GPUs

Some GPUs are **integrated**, which means they are **built into the CPU** instead of being a separate graphics card. Integrated GPUs are:

- **Energy-efficient**, so they suit **battery-powered devices** such as laptops.
- **Cost-effective**, because there is no need to buy a separate graphics card.

A **dedicated** GPU is a separate graphics card with its own VRAM. It is more powerful but costs more and uses more power.

#### What decides a GPU's speed?

| Factor | Meaning |
|--------|---------|
| **Core clock** | The speed at which the GPU cores run, in **MHz** (megahertz). It directly affects processing power. |
| **Memory clock** | The speed of the VRAM, in MHz. It shows how fast data can move between the memory and the GPU. |

### Worked Example

**Task 1 (pixels per second):** A monitor shows 1920 × 1080 pixels at 60 frames per second. How many pixel updates does the GPU handle every second?

1. Pixels per frame = 1920 × 1080 = **2,073,600**
2. Pixels per second = 2,073,600 × 60 = **124,416,000**

That is more than 124 million pixel updates every second, which is why a GPU's parallel cores are so helpful.

**Task 2 (parallel processing):** There are 100 tasks, and each takes 1 second.

| Number of cores | Time needed |
|-----------------|-------------|
| 1 core | 100 seconds |
| 10 cores | 10 seconds |
| 100 cores | 1 second |

More cores working in parallel finish the work faster.

### Activity

a. What does GPU stand for?
b. What is parallel processing?
c. How many pixels are on a 3840 × 2160 (4K) screen?
d. Name two parts inside a GPU and what each one does.
e. Why is an integrated GPU a good choice for a laptop?

<details>
<summary><b>Answer</b></summary>

a. **Graphics Processing Unit**
b. Doing **many tasks at the same time**.
c. 3840 × 2160 = **8,294,400 pixels**
d. For example: **VRAM** stores textures and frame buffers; the **rasterizer** turns 3D objects into pixels; the **frame buffer** holds the finished image.
e. It is **energy-efficient**, which helps battery life, and **cost-effective**, because no separate graphics card is needed.

</details>

---

## Stage 3 Summary

- The **motherboard** distributes power from the PSU to the CPU, memory, and peripherals, and uses **voltage regulation circuits** to keep each part's power steady.
- The **BIOS/UEFI** is firmware that **initializes the hardware** during boot and lets you change settings, such as the **boot order**.
- The **CPU** is the "brain". It is built from billions of **transistors** and repeats the **fetch-decode-execute** loop.
- The **control unit** directs the CPU's work, and the **ALU** does arithmetic and logic.
- CPU speed depends on **clock speed**, **cache** (L1, L2, L3), **bus speed**, and **threads**.
- The **GPU** is a specialized processor that uses **parallel processing** for graphics, gaming, and AI.
- A GPU's main parts are **cores, VRAM, a memory interface, shaders, a rasterizer, a frame buffer, and control logic**.
- GPU speed depends on the **core clock** and the **memory clock**. **Integrated GPUs** are energy-efficient and low in cost, while **dedicated** GPUs are more powerful.

# Stage 4: Graphics Memory, RAM, ROM, and Storage

## Learning Goals

By the end of this stage, you will be able to:

1. Identify core physical components of computers and explain basic functions.
2. Explain what VRAM is and read the main details of a graphics card.
3. Explain the difference between RAM and ROM, and where cache memory fits.
4. Describe what decides RAM performance: frequency, type, and timings.
5. Describe secondary storage devices (HDD, SSD, optical, USB flash drives, memory cards) and their strengths and weaknesses.
6. Explain how the CPU retrieves data using the fetch-decode-execute cycle and interrupts.

**Topics covered (from Internal Hardware and Ports and External Storage):**

- Graphics Card (VRAM)
- RAM
- RAM vs ROM
- USB and external storage (flash drives, memory cards)

---

# 4.1 Graphics Card: VRAM and Specs

## Explanation

A graphics card has its own fast memory called **VRAM** (Video RAM). It stores the data needed to draw pictures, such as textures and the final image before it is shown on screen.

VRAM comes in different **types**. Each new type is usually **faster at transferring data** than the one before it. For example, **GDDR6** is faster than **GDDR5**. (**GDDR** stands for Graphics Double Data Rate.) Newer types are common in modern graphics cards used for demanding jobs, such as gaming and video editing.

A **dedicated GPU** is a graphics card with its own VRAM. Here is a real example. A laptop with an **NVIDIA RTX 3050** graphics card shows these specs in the program **CPU-Z**:

| Detail | Value | What it means |
|--------|-------|---------------|
| Name | NVIDIA GeForce RTX 3050 Laptop GPU | The graphics chip's model |
| Code name | GA107 | The name of the chip's design |
| Technology | 8 nm | The size of the tiny parts inside the chip. A **nanometer (nm)** is one billionth of a meter. Smaller sizes usually mean more parts fit on the chip and it uses less power. |
| Max TDP | 80 W | The most power (and heat) the chip is designed to handle, in watts |
| GFX core clock | 210 MHz | The current speed of the GPU core (it changes depending on the workload) |
| Shader clock | 405 MHz | The current speed of the shaders, the units that handle lighting and color |
| Memory size | 4 GB | How much VRAM there is |
| Memory type | GDDR6 | The type of VRAM |
| Bus width | 128 bits | How many bits of data can move between the VRAM and the GPU at the same time |

## Worked Example

**Task:** The RTX 3050 has a **128-bit** memory bus. How many bytes can it move in one transfer, and how many transfers are needed to move 1,600 bytes?

1. 1 byte = 8 bits, so 128 bits ÷ 8 = **16 bytes per transfer**
2. 1,600 bytes ÷ 16 = **100 transfers**

A wider bus moves the same data in fewer transfers.

## Activity

a. What does VRAM store?
b. Which is the newer and faster memory type: GDDR5 or GDDR6?
c. How much VRAM does the RTX 3050 in the example have?
d. A memory bus is 256 bits wide. How many bytes can it move in one transfer?

<details>
<summary><b>Answer</b></summary>

a. Data needed for drawing images, such as **textures** and the **frame buffer**.
b. **GDDR6**
c. **4 GB**
d. 256 ÷ 8 = **32 bytes**

</details>

---

# 4.2 Storage

## Primary Storage: RAM, ROM, and Cache

### Explanation

**Storage** is the part of the computer that holds data the CPU and other components need to reach **right away** while the computer is working. There are two main groups: **primary storage** and **secondary storage**. We start with primary storage.

**RAM (Random Access Memory)** keeps data **temporarily** while the computer is running. RAM gives **very quick access** to data, but **everything in it is lost when the power goes off**. (This is called being **volatile**.) RAM acts as a **high-speed buffer**, which means a fast waiting area, between the CPU and slower storage devices such as hard drives. This lets the computer quickly reach the data it needs to run programs and carry out commands.

**ROM (Read Only Memory)** keeps data that **cannot be easily changed**. In modern computers, ROM usually holds **firmware**, which is software stored inside a hardware device to tell it how to work.

| Feature | RAM | ROM |
|---------|-----|-----|
| Full name | Random Access Memory | Read Only Memory |
| Holds | Programs and data in use right now | Firmware (start-up instructions) |
| Can it be changed easily? | Yes | No |
| When the power goes off | Contents are lost | Contents are kept |

**Where RAM sits in the computer:**

- The **motherboard** has **memory slots** for **DRAM modules**. (**DRAM** is Dynamic RAM, the common type of RAM. A **module** is a small circuit board holding the memory chips.)
- Common module types are **DDR4** and **DDR5**. They have different speeds and sizes.
- How well the memory talks to the CPU also depends on the motherboard's **chipset** and **bus speed**.

**Cache memory:** In modern computers, the CPU usually has **cache memory**. It is a **smaller and faster** type of volatile memory **very close to the CPU**, and it keeps the most frequently used data so the CPU can reach it even faster than RAM.

### Worked Example

**Task:** Decide where each item is kept.

| Item | Where | Why |
|------|-------|-----|
| A game while you are playing it | RAM | Needs fast access, and is only needed while it runs |
| The instructions a computer uses to start up | ROM | They must stay when the power is off |
| The data the CPU uses again and again | Cache | Fastest access, right next to the CPU |

### Activity

a. Which memory loses its contents when the computer is switched off, RAM or ROM?
b. What does "buffer" mean when we say RAM is a high-speed buffer?
c. Name two RAM module types.
d. Where is cache memory located?

<details>
<summary><b>Answer</b></summary>

a. **RAM**
b. A **fast waiting area** between the CPU and slower storage, where data is held for quick access.
c. **DDR4** and **DDR5**
d. **Very close to the CPU** (inside or right next to it).

</details>

---

## RAM Performance

### Explanation

RAM performance is usually described using three things:

| Term | Meaning |
|------|---------|
| **RAM frequency** | How fast the RAM can **read and write** data, measured in **MHz** (megahertz, millions of cycles per second), for example 3200 MHz. A higher frequency means faster data transfer between the RAM and the CPU. |
| **RAM type** | The technology **generation**, such as DDR4 or DDR5. Newer types are usually faster and more efficient. |
| **RAM timings** | Numbers that show **latency**, which is the **delay** before data starts to arrive. **Lower numbers mean faster performance.** |

Here are the main details of a real RAM module, as shown in **CPU-Z**:

| Detail | Value | What it means |
|--------|-------|---------------|
| Type | DDR4 | The RAM generation |
| Size | 8 GB | The amount of memory |
| Channel | 1 × 64-bit | How data travels to the CPU: one path that is 64 bits wide |
| DRAM frequency | 1596.1 MHz | The speed of the RAM's clock |
| CAS latency (CL) | 22 clocks | The delay, counted in clock cycles, before data can be read. This is the best-known timing number. |
| RCD, RP, RAS, RC | 22, 22, 52, 74 clocks | Other timing numbers for opening and closing parts of the memory |
| Command rate | 1T | How quickly the memory accepts commands |

*(DDR memory sends data twice per clock cycle. That is why a clock of about 1600 MHz is sold as "3200" memory.)*

### Worked Example

**Task:** Which RAM responds faster? Both modules run at 1596.1 MHz. Module A has CL = 22, and Module B has CL = 16.

1. One clock cycle lasts 1 ÷ 1596.1 million seconds, which is about **0.627 nanoseconds** (a **nanosecond** is one billionth of a second).
2. Module A: 22 × 0.627 ≈ **13.8 ns**
3. Module B: 16 × 0.627 ≈ **10.0 ns**

Module B has a **lower timing number**, so it has less delay and is **faster**.

### Activity

a. What does a lower timing number mean?
b. Which gives faster transfer: 2666 MHz or 3200 MHz RAM (same type)?
c. How much RAM is in the CPU-Z example?
d. Name the two RAM generations mentioned in this section.

<details>
<summary><b>Answer</b></summary>

a. **Less delay**, so faster performance.
b. **3200 MHz** (a higher frequency means faster transfer).
c. **8 GB**
d. **DDR4** and **DDR5**

</details>

---

## Secondary Storage and USB Drives

### Explanation

**Secondary storage** is **permanent** storage. It includes hard drives (HDD), solid-state drives (SSD), optical drives, and USB flash drives. Data **stays stored** here even when the computer is turned off.

| Device | How it works | Notes |
|--------|--------------|-------|
| **Hard Disk Drive (HDD)** | A traditional drive that stores large amounts of data on **spinning magnetic disks** called **platters** | Big capacity, slower, has moving parts |
| **Solid-State Drive (SSD)** | **Flash-based** storage (it uses electronic memory chips) with **no moving parts** | Much faster than an HDD |
| **Optical storage** | Discs such as **CDs, DVDs, and Blu-rays**, read by a laser | Used for media and backup copies |
| **USB flash drive** | A **portable, solid-state** storage device that plugs into a **USB port** | Used to move files between devices and for backups. Capacity ranges from a few gigabytes to several terabytes. |

A **memory card**, such as an **SD card**, is another small, portable flash storage device. It is commonly used in cameras and phones.

**Advantages of USB drives:**

- **Portability**: Small and light, so they are easy to carry.
- **Plug-and-play**: No installation is needed. You plug the drive into a USB port and it is ready to use.

**Disadvantages of USB drives:**

- **Limited lifespan**: Flash storage can only be written a limited number of times (called **write cycles**). For most people this does not matter unless the drive is used very heavily.
- **Easy to lose or damage**: Because they are so small, they can be misplaced or damaged if not handled carefully.

### Worked Example

**Task:** Choose the best storage for each need.

| Need | Best choice | Why |
|------|-------------|-----|
| Carry a school project to another computer | USB flash drive | Portable and plug-and-play |
| Make a computer start and open programs quickly | SSD | Fast, with no moving parts |
| Store a large archive of old files cheaply | HDD | Large capacity |
| Keep the photos from a camera | Memory card (SD card) | Small, made for cameras |

### Activity

a. Which type of drive has spinning platters?
b. Give one advantage and one disadvantage of USB drives.
c. What is a write cycle?

<details>
<summary><b>Answer</b></summary>

a. The **HDD** (hard disk drive).
b. Advantage: for example, **portability** or **plug-and-play**. Disadvantage: for example, a **limited lifespan** or **easy to lose or damage**.
c. **One time data is written** to the flash storage. Flash storage can only handle a limited number of them.

</details>

---

## Data Access and Retrieval

### Explanation

Primary and secondary storage work together:

- **Primary storage (RAM)** is **much faster** than secondary storage, so the CPU can reach data quickly while it works. But because it is **volatile**, it needs a **constant power supply**. That is why data that is not in active use is **moved to secondary storage**.
- **Secondary storage** has **much more space** and keeps data for the long term, but it has **slower access**. It is used for saving documents, system files, applications, and **databases** (organized collections of data).

**How the CPU retrieves data: the fetch-decode-execute cycle**

| Step | What happens |
|------|--------------|
| **Fetch** | The CPU gets the instruction or data from memory |
| **Decode** | The CPU works out what action the instruction asks for |
| **Execute** | The CPU does the action, such as adding numbers or moving data |

**Input/Output (I/O) and interrupts**

I/O devices (like a keyboard or printer) send and receive data using **interrupts**. An **interrupt** is a **signal that pauses** the CPU's normal work so it can **handle an input or output task**. After that, the CPU **returns to the cycle** where it left off.

### Worked Example

**Task:** You are running a program, and you press a key.

| Step | What happens |
|------|--------------|
| 1 | The CPU is in the middle of the fetch-decode-execute cycle for your program |
| 2 | The keyboard sends an **interrupt** signal |
| 3 | The CPU **pauses** the program and handles the key press (the input task) |
| 4 | The CPU **returns** to the cycle and carries on with the program |

### Activity

a. Why is data not in use moved from RAM to secondary storage?
b. Which has more storage space, primary or secondary storage?
c. What does an interrupt do?
d. Put in order: **Execute**, **Fetch**, **Decode**.

<details>
<summary><b>Answer</b></summary>

a. RAM is **volatile** and needs constant power, so data that must be kept is moved to **secondary storage**, which keeps it without power.
b. **Secondary storage**
c. It **pauses the CPU's normal processing** so it can handle an input or output task, then the CPU returns to the cycle.
d. **Fetch → Decode → Execute**

</details>

---

## Stage 4 Summary

- **VRAM** is the graphics card's own memory. Newer types (like **GDDR6**) are faster than older ones (like GDDR5). A **128-bit** bus moves 16 bytes per transfer.
- **RAM** is fast, temporary memory that loses its contents without power. **ROM** keeps **firmware** that cannot be easily changed. **Cache** is small, very fast memory near the CPU.
- **RAM performance** depends on **frequency** (MHz), **type** (DDR4 or DDR5), and **timings** (lower means less delay).
- **Secondary storage** keeps data without power: **HDD** (spinning platters), **SSD** (flash, no moving parts), **optical discs**, **USB flash drives**, and **memory cards**.
- **USB drives** are portable and plug-and-play, but they have a limited number of write cycles and are easy to lose or damage.
- **RAM** is faster and **secondary storage** is larger and permanent, so data not in use is moved to secondary storage.
- The CPU retrieves data using **fetch-decode-execute**. **Interrupts** pause that cycle so the CPU can handle input and output.