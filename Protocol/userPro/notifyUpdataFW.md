![wpiLogo](../../images/wpiLogo.jpg)
# 5.2.11.通知 BootLoader 设备更新 FW 版本

### Set Report 数据格式
<table>
    <tr>
        <th white-space : nowrap> Byte \ Bit</th>
        <th> 7 </th>
        <th> 6 </th>
        <th> 5 </th>
        <th> 4 </th>
        <th> 3 </th>
        <th> 2 </th>
        <th> 1 </th>
        <th> 0 </th>
    </tr>
    <tr>
        <th> 0 </th>
        <th colspan = "8" align = "left"> [ OUT ] Reprot ID = 0x01</th>
    </tr>
    <tr>
        <th> 1 </th>
        <th colspan = "8" align = "left"> [ OUT ] CMD Status = 0x00</th>
    </tr>
    <tr>
        <th> 2 </th>
        <th colspan = "8" align = "left"> [ OUT ] CMD ID = 0x50</th>
    </tr>
    <tr>
        <th> 3 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data_Index ( LSB ) = 0x00</th>
    </tr>
    <tr>
        <th> 4 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data_Index ( MSB ) = 0x00</th>
    </tr>
    <tr>
        <th> 5 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data_Length = 4 </th>
    </tr>
    <tr>
        <th> 6 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data 0 ( FW 数据的字节数, unsigned int 的第 1 个 Byte )</th>
    </tr>
    <tr>
        <th> 7 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data 1 ( FW 数据的字节数, unsigned int 的第 2 个 Byte )</th>
    </tr>
    <tr>
        <th> 8 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data 2 ( FW 数据的字节数, unsigned int 的第 3 个 Byte )</th>
    </tr>
    <tr>
        <th> 9 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data 3 ( FW 数据的字节数, unsigned int 的第 4 个 Byte )</th>
    </tr>
    <tr>
        <th> ...... </th>
        <th colspan = "8" align = "left"> [ OUT ] Data = 0x00 </th>
    </tr>
    <tr>
        <th> 63 </th>
        <th colspan = "8" align = "left"> [ OUT ] CheckSum: CheckSum = 55h - ( Byte0 + ... + Byte62 ) & 0xFF</th>
    </tr>
</table>

### Get Report 数据格式
<table>
    <tr>
        <th white-space : nowrap> Byte \ Bit</th>
        <th> 7 </th>
        <th> 6 </th>
        <th> 5 </th>
        <th> 4 </th>
        <th> 3 </th>
        <th> 2 </th>
        <th> 1 </th>
        <th> 0 </th>
    </tr>
    <tr>
        <th> 0 </th>
        <th colspan = "8" align = "left"> [ IN ] Reprot ID = 0x01</th>
    </tr>
    <tr>
        <th> 1 </th>
        <th colspan = "8" align = "left" white-space : nowrap> [ IN ] CMD Status = 0x00 ( Sucess ) ; 0x01 ( Busy ) ; 0x02 ( Fail ) ; 0x03 ( Not Support )</th>
    </tr>
    <tr>
        <th> 2 </th>
        <th colspan = "8" align = "left"> [ IN ] CMD ID = 0x50</th>
    </tr>
    <tr>
        <th> 3 </th>
        <th colspan = "8" align = "left"> [ IN ] Data_Index ( LSB ) = 0x00</th>
    </tr>
    <tr>
        <th> 4 </th>
        <th colspan = "8" align = "left"> [ IN ] Data_Index ( MSB ) = 0x00</th>
    </tr>
    <tr>
        <th> 5 </th>
        <th colspan = "8" align = "left"> [ IN ] Data_Length = 0 </th>
    </tr>
    <tr>
        <th> ...... </th>
        <th colspan = "8" align = "left"> [ IN ] Data = 0x00 </th>
    </tr>
    <tr>
        <th> 63 </th>
        <th colspan = "8" align = "left"> [ IN ] CheckSum: CheckSum = 55h - ( Byte0 + ... + Byte62 ) & 0xFF</th>
    </tr>
</table>