# chapter3 UDP
## 库元件及其调用
udp(User-Defined primitives) Verilog 中预先定义的基本逻辑单元称为原语，即现成的门级库元件，包括：and、nand、or、xor、not等。这些门有一个到多个输入端口，但只有一个输出口，且输出口排在最左侧
## 用户自定义原语
用户自定义的基础元件，关键词 table_endtable 将引导出该 UDP逻辑功能真值表。