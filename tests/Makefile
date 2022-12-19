SIM ?= icarus
TOPLEVEL_LANG ?= verilog
VERILOG_SOURCES += $(PWD)/../hdl/dut.v
VERILOG_SOURCES += $(PWD)/wrappers/hdl/xor_test.v
VERILOG_SOURCES += $(PWD)/wrappers/hdl/ifc_test.v
VERILOG_SOURCES += $(PWD)/../hdl/ifc_xor.v
VERILOG_SOURCES += $(PWD)/../hdl/FIFO1.v
VERILOG_SOURCES += $(PWD)/../hdl/FIFO2.v
all:xor ifc
xor:
         rm -rf sim_build
         $(MAKE) sim MODULE=xor_test TOPLEVEL=xor_test
ifc:
         rm -rf sim_build
          $(MAKE) sim MODULE=ifc_test TOPLEVEL=ifc_test
TOPLEVEL = dut
MODULE = dut_test
include $(shell cocotb-config --makefiles)/Makefile.sim
