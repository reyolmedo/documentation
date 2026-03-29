.. _ad7405 user-guide:

User guide
===============================================================================

The complete user guides of the evaluation boards can be found at:

- :adi:`EVAL-AD7405 User Guide (UG-690) <https://www.analog.com/media/en/technical-documentation/user-guides/EVAL-AD7405FMCZ_UG-690.pdf>`

Hardware guide
-------------------------------------------------------------------------------
Hardware configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The :adi:`EVAL-AD7405` board connect to the FPGA
carrier via the FMC LPC connector.

Refer to the :ref:`ad7405 quickstart ad7405_sdp_h1` quick start guide for the exact jumper
and switch settings corresponding to the selected boot mode.

Power supply
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The evaluation board is powered through the FMC LPC
connector when attached to the EVAL-SDP-CH1Z FPGA carrier board.
No additional power supply is required for normal operation.

The FMC interface uses a **3.3 V** VADJ supplied by the carrier board,
which provides the digital supply (VDD2) for the AD7405 by default.

Alternative power configurations are supported through on-board
connectors. The analog supply (VDD1) may be sourced from the on-board
isolated dc-to-dc converter, from an external 5 V supply, or from a
high-voltage external input that is regulated on board. The digital
supply (VDD2) may also be provided by an external supply when operating
in standalone mode.

Analog inputs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The EVAL-AD7405FMCZ evaluation board provides differential analog
input connections for the AD7405 through on-board input connectors.
The VIN+ and VIN– signals are routed directly to the ADC input pins.

Link options are provided to short either VIN+ or VIN– to ground for
setup and diagnostic purposes. These links must be removed when an
external input signal is applied to the corresponding input.

Schematic, PCB Layout, Bill of Materials
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Design files (schematics, PCB layout, and BOM) are available from the
respective product pages:

- :adi:`EVAL-AD7405`

Software guide
-------------------------------------------------------------------------------

The evaluation board are supported through the :ref:`libiio` library, which
is cross-platform (Windows, Linux, Mac) with bindings for C, C#, Python,
MATLAB, and others. Applications that interface via libiio include:

- :ref:`iio-oscilloscope` — graphical waveform and spectrum analyzer
- :external+scopy:doc:`Scopy <index>` v2.0 or later (requires the IIO plugin)
- :external+pyadi-iio:doc:`index` — Python interface

For a step-by-step walkthrough of connecting and using these tools with the
:adi:`EVAL-AD7405` on the SDP-H1, see the
:ref:`ad7405 quickstart sdp_h1` guide.