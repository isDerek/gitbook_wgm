![wpiLogo](../../images/wpiLogo.jpg)
# 5.1.1.获取设备 MAC 地址

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
        <th colspan = "8" align = "left"> [ OUT ] CMD ID = 0x01</th>
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
        <th colspan = "8" align = "left"> [ IN ] CMD ID = 0x01</th>
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
        <th colspan = "8" align = "left"> [ IN ] Data_Length = 6 </th>
    </tr>
    <tr>
        <th> 6 </th>
        <th colspan = "8" align = "left"> [ IN ] MAC 地址第 1 位 </th>
    </tr>
    <tr>
        <th> 7 </th>
        <th colspan = "8" align = "left"> [ IN ] MAC 地址第 2 位 </th>
    </tr>
    <tr>
        <th> 8 </th>
        <th colspan = "8" align = "left"> [ IN ] MAC 地址第 3 位 </th>
    </tr>
    <tr>
        <th> 9 </th>
        <th colspan = "8" align = "left"> [ IN ] MAC 地址第 4 位 </th>
    </tr>
    <tr>
        <th> 10 </th>
        <th colspan = "8" align = "left"> [ IN ] MAC 地址第 5 位 </th>
    </tr>
    <tr>
        <th> 11 </th>
        <th colspan = "8" align = "left"> [ IN ] MAC 地址第 6 位 </th>
    </tr>
    <tr>
        <th> 12 </th>
        <th colspan = "8" align = "left"> [ IN ] CheckSum: CheckSum = 55h - ( Byte1 + ... + Byte11 ) & 0xFF</th>
    </tr>
    <tr>
        <th> 13 </th>
        <th colspan = "8" align = "left"> [ IN ] 0x29 (")")</th>
    </tr>
</table>