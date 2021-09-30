Directory Layout of Egalito
============================

In this section, we describe some relevant directories within Egalito. The ``src`` folder contains the source code of Egalito and the ``app`` folder contains applications created using Egalito including ``etshell``, which is a shell that can run Egalito's functionalities and passes and ``etelf`` which is a tool that for code transformation.

The subdirectories within the ``src`` directory are :

``analysis`` : Contains analyses like control flow graph generation, data flow analysis, usedef analysis, jump table detection etc.

``chunk`` : Contains the implementations for the `Chunk <chunk.html>`_ hierarchy.

``conductor`` : Contains the highest level interfaces (API) for the user. Particularly useful are Interface in `src/conductor/interface.h <https://github.com/columbia/egalito/blob/master/src/conductor/interface.h>`_ and ConductorSetup in `src/conductor/setup.h <https://github.com/columbia/egalito/blob/master/src/conductor/setup.h>`_.

``disasm`` : Low-level disassembly library integration, supporting Capstone (with Distorm3 on x86) and a RISC-V disassembler.

- `Disassemble::instruction` in `src/disasm/disassemble.h <https://github.com/columbia/egalito/blob/master/src/disasm/disassemble.h>`_ uses the correct disassembly library. There are higher-level disassembly operations too (like functions).
- `Reassemble::instruction` in `src/disasm/reassemble.h <https://github.com/columbia/egalito/blob/master/src/disasm/reassemble.h>`_ allows new instructions to be specified as strings (note: requires `USE_KEYSTONE=1` in the Makefile).

``elf`` :

``generate`` :

``instr`` : Contains implementations of different types of instructions including control flow instruction, linked instruction, isolated instruction etc.

``log`` : Contains implementation of the logging feature

``operation`` :

``pass`` : Contains the different passes that can be run on Egalito

``transform`` : Contains the code for transformation




