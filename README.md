# Synopsys Design Compiler Configuration

This repository contains the setup files for synthesizing a design using Synopsys Design Compiler.

```text
project_root/
├── rtl/                # Place your RTL (Verilog/VHDL) source files here
├── top_settings.tcl    # Edit this file with your design-specific data
├── work/               # Run synthesis from this directory
│   └── Makefile        # Automation for clean and synthesis steps
├── reports/            # Generated synthesis and timing reports (created after synthesis)
└── output/             # Synthesized netlists and related outputs (created after synthesis)
```

## To do

Please follow the instructions below:

0. Source `pd.sh` from the `pd_tools` mounted.
   ```bash
   source /tools/pd_tools/pd.sh
   ```
1. Copy the RTL design files to the `rtl` directory.
2. Update the `top_settings.tcl` with the top module name, clock_name, clock_period of the design and the path for the technology library.
3. Go to `work` directory and do the following:
   * For initialising: `make clean`
   * For Synthesis: `make syn`

Once the synthesis is complete, the reports and output directory will be created and can be reviewed.
