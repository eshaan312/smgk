# Simple Multi-core Graphical Kernel
Built by Eshaan Deshmukh
# What it is?
It's a WIP project developing a 3D ray tracer using multi-core bare metal x86 Netwide Assembly.
# How does it work?
It includes a bootloader and detecting, booting, and handling all available extra CPU cores using APIC, SMP and my custom spinlock system. Each core was given a field of static memory to use to render graphics. After setting up the environment to work in, I started work on the ray tracer for the graphics. Throughout this process, I heavily utilized my CPU’s AVX2 instructions, specifically the ones concerning SIMD registers (x/ymm0, x/ymm1, …) including VSHUFPS, VBROADCASTSS, and VCVTDQ2PS. This allowed me to speed up the program by up to 400%.
