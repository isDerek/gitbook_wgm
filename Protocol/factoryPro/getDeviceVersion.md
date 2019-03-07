![wpiLogo](../../images/wpiLogo.jpg)

# 5.1.2.获取设备版本号

---

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
        <th colspan = "8" align = "left"> [ OUT ] 0x28 ("(") </th>
    </tr>
    <tr>
        <th> 1 </th>
        <th colspan = "8" align = "left"> [ OUT ] CMD ID = 0x02</th>
    </tr>
    <tr>
        <th> 2 </th>
        <th colspan = "8" align = "left"> [ OUT ] Device ID = 0x01 ( Dongle 设备 )、0x02 ( Mouse 设备 ) </th>
    </tr>
    <tr>
        <th> 3 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data_Index ( LSB ) = 0x00 </th>
    </tr>
    <tr>
        <th> 4 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data_Index ( MSB ) = 0x00 </th>
    </tr>
    <tr>
        <th> 5 </th>
        <th colspan = "8" align = "left"> [ OUT ] Data_Length = 0 </th>
    </tr>
    <tr>
        <th> 6 </th>
        <th colspan = "8" align = "left"> [ OUT ] CheckSum: CheckSum = 55h - ( Byte1 + ... + Byte5 ) & 0xFF</th>
    </tr>
    <tr>
        <th> 7 </th>
        <th colspan = "8" align = "left"> [ OUT ] 0x29 (")")</th>
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
        <th colspan = "8" align = "left"> [ IN ] 0x28 ("(") </th>
    </tr>
    <tr>
        <th> 1 </th>
        <th colspan = "8" align = "left"> [ IN ] CMD ID = 0x02</th>
    </tr>
    <tr>
        <th> 2 </th>
        <th colspan = "8" align = "left"> [ IN ] Device ID = 0x01 ( Dongle 设备 )、0x02 ( Mouse 设备 ) </th>
    </tr>
    <tr>
        <th> 3 </th>
        <th colspan = "8" align = "left"> [ IN ] Data_Index ( LSB ) = 0x00 </th>
    </tr>
    <tr>
        <th> 4 </th>
        <th colspan = "8" align = "left"> [ IN ] Data_Index ( MSB ) = 0x00 </th>
    </tr>
    <tr>
        <th> 5 </th>
        <th colspan = "8" align = "left"> [ IN ] Data_Length = X </th>
    </tr>
    <tr>
        <th> ... </th>
        <th colspan = "8" align = "left"> [ IN ] 版本号形式未确定 </th>
    </tr>
    <tr>
        <th> ...+1 </th>
        <th colspan = "8" align = "left"> [ IN ] CheckSum: CheckSum = 55h - ( Byte1 + ... + Byte... ) & 0xFF</th>
    </tr>
    <tr>
        <th> ...+2 </th>
        <th colspan = "8" align = "left"> [ IN ] 0x29 (")")</th>
    </tr>
</table>
