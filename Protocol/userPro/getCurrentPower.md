![wpiLogo](../../images/wpiLogo.jpg)
# 5.2.9.获取当前电量

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
        <th colspan = "8" align = "left"> [ OUT ] Reprot ID ( Reserved ) </th>
    </tr>
    <tr>
        <th> 1 </th>
        <th colspan = "8" align = "left"> [ OUT ] CMD Status = 0x00</th>
    </tr>
    <tr>
        <th> 2 </th>
        <th colspan = "8" align = "left"> [ OUT ] CMD ID = 0x0D </th>
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
        <th colspan = "8" align = "left"> [ IN ] Reprot ID ( Reserved )</th>
    </tr>
    <tr>
        <th> 1 </th>
        <th colspan = "8" align = "left" white-space : nowrap> [ IN ] CMD Status = 0x00 ( Sucess ) ; 0x01 ( Busy ) ; 0x02 ( Fail ) ; 0x03 ( Not Support )</th>
    </tr>
    <tr>
        <th> 2 </th>
        <th colspan = "8" align = "left"> [ IN ] CMD ID = 0x0D </th>
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
        <th colspan = "8" align = "left"> [ IN ] Data_Length = 2 </th>
    </tr>
    <tr>
        <th> 6 </th>
        <th colspan = "8" align = "left"> [ IN ] Data = ( 采集电量的字节数，unsigned int 第一个 Byte ) </th>
    </tr>
    <tr>
        <th> 7 </th>
        <th colspan = "8" align = "left"> [ IN ] Data = ( 采集电量的字节数，unsigned int 第二个 Byte ) </th>
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