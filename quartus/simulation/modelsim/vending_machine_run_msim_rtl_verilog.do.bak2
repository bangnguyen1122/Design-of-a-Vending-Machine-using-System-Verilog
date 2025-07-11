transcript on
if {[file exists rtl_work]} {
	vdel -lib rtl_work -all
}
vlib rtl_work
vmap work rtl_work

vlog -sv -work work +incdir+D:/Projects_Upload_to_Github/Design-of-a-Vending-Machine-using-System-Verilog-master/src {D:/Projects_Upload_to_Github/Design-of-a-Vending-Machine-using-System-Verilog-master/src/vending_machine.sv}

vlog -sv -work work +incdir+D:/Projects_Upload_to_Github/Design-of-a-Vending-Machine-using-System-Verilog-master/quartus/../tb {D:/Projects_Upload_to_Github/Design-of-a-Vending-Machine-using-System-Verilog-master/quartus/../tb/vending_machine_tb.sv}

vsim -t 1ps -L altera_ver -L lpm_ver -L sgate_ver -L altera_mf_ver -L altera_lnsim_ver -L cyclonev_ver -L cyclonev_hssi_ver -L cyclonev_pcie_hip_ver -L rtl_work -L work -voptargs="+acc"  vending_machine_tb

add wave *
view structure
view signals
run -all
