# 基于CCE集群<a name="bcs_usermanual_0014"></a>

Hyperledger Fabric增强版服务支持在CCE集群和边缘集群上部署。本页面介绍如何部署基于CCE集群的Hyperledger Fabric增强版服务。

-   基于CCE集群部署：服务实例和区块链数据均存储在华为云上，当您没有可用的自有硬件资源时，可购买华为云资源并采用此方式部署。

    >![](public_sys-resources/icon-notice.gif) **须知：** 
    >BCS服务需要独占CCE集群，部署BCS服务前请确保CCE集群未被使用。

-   基于边缘集群部署：区块链数据存储在您的自有节点上，即边缘节点上，BCS只提供区块链管理能力。当您已经有了可用的硬件资源时，为了减少资源浪费、降低您的投入成本，可采用此方式部署。

## 前提条件<a name="section130811619373"></a>

如果您使用华为云帐号创建的IAM用户进行操作，IAM用户需要具备足够的权限才能操作并订购区块链服务。具体操作请参见：[权限管理](权限管理.md)。

您可以通过先创建用户组并授权再将用户加入到用户组的方式，使用户具有用户组中的权限。

## 部署区块链服务<a name="zh-cn_topic_0094520206_section3843378016187"></a>

完成环境准备工作后，可按照如下步骤购买并部署区块链服务。

>![](public_sys-resources/icon-note.gif) **说明：** 
>现网帐号欠费会导致服务网盘被释放，已购买的服务不可用。

1.  购买区块链服务。
    -   登录区块链服务管理控制台，进入“服务管理”，单击Hyperledger Fabric增强版的“购买”按钮。
    -   未部署可信计算插件的区块链服务，可选择添加可信计算插件，请执行以下步骤添加可信计算插件：

        1.  登录区块链服务管理控制台。
        2.  单击左侧导航栏中的“插件管理”。
        3.  在“插件仓库“页签下的可信插件卡片中，单击“安装“。

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >-   已部署的区块链服务需要先升级到最新的版本，才可以添加可信计算。
        >-   已部署的服务，单击左侧导航栏中的“服务管理”，单击右侧的“操作记录”，查看操作记录并在服务右侧进行“操作详情”及“删除”操作。


2.  根据界面提示，配置区块链基本信息，参数如[表1](#table11911152765220)所示。

    **表 1**  基本信息配置

    <a name="table11911152765220"></a>
    <table><thead align="left"><tr id="row189131327125210"><th class="cellrowborder" valign="top" width="21.92%" id="mcps1.2.4.1.1"><p id="p8914152775212"><a name="p8914152775212"></a><a name="p8914152775212"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.080000000000005%" id="mcps1.2.4.1.2"><p id="p191452795212"><a name="p191452795212"></a><a name="p191452795212"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.4.1.3"><p id="p791419273527"><a name="p791419273527"></a><a name="p791419273527"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row10914142785216"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p244483414215"><a name="p244483414215"></a><a name="p244483414215"></a>计费模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p444483413422"><a name="p444483413422"></a><a name="p444483413422"></a>区块链服务管理费收费模式，支持包年/包月、按需计费。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p04441434154211"><a name="p04441434154211"></a><a name="p04441434154211"></a>包年/包月</p>
    </td>
    </tr>
    <tr id="row10914102718522"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p944511343421"><a name="p944511343421"></a><a name="p944511343421"></a>区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p1445034104215"><a name="p1445034104215"></a><a name="p1445034104215"></a>区块链基础设施所在的区域，建议选择与业务应用系统相同的地域。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p344515348420"><a name="p344515348420"></a><a name="p344515348420"></a>使用默认区域</p>
    </td>
    </tr>
    <tr id="row98014253458"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p481122574518"><a name="p481122574518"></a><a name="p481122574518"></a>企业项目</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p5953725164715"><a name="p5953725164715"></a><a name="p5953725164715"></a>请选择已创建的企业项目，将区块链服务添加至企业项目中。</p>
    <div class="note" id="note1027118381486"><a name="note1027118381486"></a><a name="note1027118381486"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul1745154235117"></a><a name="ul1745154235117"></a><ul id="ul1745154235117"><li>如果您没有开通企业管理服务，将无法看到企业项目选项。<p id="p164091642173416"><a name="p164091642173416"></a><a name="p164091642173416"></a>开通方法请参见<a href="https://support.huaweicloud.com/usermanual-em/pm_topic_0002.html" target="_blank" rel="noopener noreferrer">如何开通企业项目</a>。</p>
    </li><li>如果您使用已有CCE集群部署区块链服务，建议您将区块链服务添加至CCE集群的企业项目中，如果区块链服务与部署区块链服务的CCE集群处于不同的企业项目，可能导致使用异常。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p23615371152"><a name="p23615371152"></a><a name="p23615371152"></a>default</p>
    </td>
    </tr>
    <tr id="row109151027185215"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p15445163416423"><a name="p15445163416423"></a><a name="p15445163416423"></a>区块链服务名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p5445203404217"><a name="p5445203404217"></a><a name="p5445203404217"></a>支持中英文字符、数字及中划线，不能以中划线开头，长度为4-24个字符。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p1744503420426"><a name="p1744503420426"></a><a name="p1744503420426"></a>bcs-wh</p>
    </td>
    </tr>
    <tr id="row1291552716526"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p344573419428"><a name="p344573419428"></a><a name="p344573419428"></a>版本类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p1844543417421"><a name="p1844543417421"></a><a name="p1844543417421"></a>BCS提供基础版、专业版、企业版和铂金版供您选择。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p1444573410423"><a name="p1444573410423"></a><a name="p1444573410423"></a>企业版</p>
    </td>
    </tr>
    <tr id="row2091582725220"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p244593411423"><a name="p244593411423"></a><a name="p244593411423"></a>区块链类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p17445163413422"><a name="p17445163413422"></a><a name="p17445163413422"></a>私有链指仅本租户内部使用的区块链服务，联盟链指可邀请其他租户一起组建联盟的区块链服务。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p335317233210"><a name="p335317233210"></a><a name="p335317233210"></a>私有链</p>
    </td>
    </tr>
    <tr id="row19504349114915"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p187154194616"><a name="p187154194616"></a><a name="p187154194616"></a>Fabric内核</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p287194154614"><a name="p287194154614"></a><a name="p287194154614"></a>区块链服务的版本号。</p>
    <p id="p1975910389312"><a name="p1975910389312"></a><a name="p1975910389312"></a>区块链版本4.x.x对应社区Hyperledger Fabric v2.2。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p106982029113012"><a name="p106982029113012"></a><a name="p106982029113012"></a>v2.2</p>
    </td>
    </tr>
    <tr id="row674219421144"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p1744503416429"><a name="p1744503416429"></a><a name="p1744503416429"></a>共识策略</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p195781176546"><a name="p195781176546"></a><a name="p195781176546"></a>区块链网络中节点之间达成共识需要遵从的规则。</p>
    <p id="p11281178165419"><a name="p11281178165419"></a><a name="p11281178165419"></a>支持快速拜占庭容错共识算法(FBFT)、Raft(CFT)，各策略分别具有不同的特性及使用场景，请参见<a href="https://support.huaweicloud.com/productdesc-bcs/bcs_productdesc_0002.html" target="_blank" rel="noopener noreferrer">产品功能</a>。</p>
    <div class="note" id="note9559239193416"><a name="note9559239193416"></a><a name="note9559239193416"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p852416121262"><a name="p852416121262"></a><a name="p852416121262"></a>raft共识基础版默认1个orderer共识节点，专业版、企业版、铂金版默认3个orderer节点。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p19307182313213"><a name="p19307182313213"></a><a name="p19307182313213"></a>快速拜占庭容错共识算法(FBFT)</p>
    </td>
    </tr>
    <tr id="row8881428111517"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p14445193418427"><a name="p14445193418427"></a><a name="p14445193418427"></a>资源初始密码</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p20445133411427"><a name="p20445133411427"></a><a name="p20445133411427"></a>登录区块链管理界面时的admin账户的密码、云主机的root密码和CouchDB密码。</p>
    <p id="p158951915563"><a name="p158951915563"></a><a name="p158951915563"></a>登录区块链管理界面时的admin账户的密码、云主机的root密码和CouchDB密码为选填项、如果您填写了就以填写值为准、如果您不填写就以资源初始密码的值为准。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p15475193463218"><a name="p15475193463218"></a><a name="p15475193463218"></a>-</p>
    </td>
    </tr>
    <tr id="row159571230121519"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p104451934134218"><a name="p104451934134218"></a><a name="p104451934134218"></a>资源初始密码确认</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p1044533415429"><a name="p1044533415429"></a><a name="p1044533415429"></a>再次输入资源初始密码进行确认。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p84452342420"><a name="p84452342420"></a><a name="p84452342420"></a>-</p>
    </td>
    </tr>
    <tr id="row1165202194315"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p99245174918"><a name="p99245174918"></a><a name="p99245174918"></a>购买时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p139235134919"><a name="p139235134919"></a><a name="p139235134919"></a>选择区块链服务的购买时长。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p39216515494"><a name="p39216515494"></a><a name="p39216515494"></a>一个月</p>
    </td>
    </tr>
    </tbody>
    </table>

3.  （可选）单击“快速创建”，系统将按照[表2](#table08701215185213)为您快速购买区块链服务。

    **表 2**  默认规格

    <a name="table08701215185213"></a>
    <table><thead align="left"><tr id="row0867101515214"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.1"><p id="p12866115125214"><a name="p12866115125214"></a><a name="p12866115125214"></a>-</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.2"><p id="p118661515165218"><a name="p118661515165218"></a><a name="p118661515165218"></a>基础版</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.3"><p id="p486618159528"><a name="p486618159528"></a><a name="p486618159528"></a>专业版</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.4"><p id="p10866181595211"><a name="p10866181595211"></a><a name="p10866181595211"></a>企业版</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.5"><p id="p17867161515216"><a name="p17867161515216"></a><a name="p17867161515216"></a>铂金版</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row17867615155217"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p886719156525"><a name="p886719156525"></a><a name="p886719156525"></a>购买CCE集群节点数</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p5867215115210"><a name="p5867215115210"></a><a name="p5867215115210"></a>1</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p3867111555211"><a name="p3867111555211"></a><a name="p3867111555211"></a>1</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p178671315145220"><a name="p178671315145220"></a><a name="p178671315145220"></a>2</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p1886710159529"><a name="p1886710159529"></a><a name="p1886710159529"></a>4</p>
    </td>
    </tr>
    <tr id="row986871585214"><td class="cellrowborder" rowspan="2" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p1986721555216"><a name="p1986721555216"></a><a name="p1986721555216"></a>CCE节点规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p1686771515528"><a name="p1686771515528"></a><a name="p1686771515528"></a>4核8GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p19867191575212"><a name="p19867191575212"></a><a name="p19867191575212"></a>4核8GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p5867815135217"><a name="p5867815135217"></a><a name="p5867815135217"></a>4核8GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p1886731510528"><a name="p1886731510528"></a><a name="p1886731510528"></a>16核32GB</p>
    </td>
    </tr>
    <tr id="row38680159526"><td class="cellrowborder" colspan="4" valign="top" headers="mcps1.2.6.1.2 mcps1.2.6.1.3 mcps1.2.6.1.4 mcps1.2.6.1.5 "><p id="p48681615115213"><a name="p48681615115213"></a><a name="p48681615115213"></a>（说明：如果默认规格售罄，则会默认购买其他较高规格。）</p>
    </td>
    </tr>
    <tr id="row98684159526"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p1868111518522"><a name="p1868111518522"></a><a name="p1868111518522"></a>CCE集群是否高可用</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p48689159524"><a name="p48689159524"></a><a name="p48689159524"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p198681515165213"><a name="p198681515165213"></a><a name="p198681515165213"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p158682156524"><a name="p158682156524"></a><a name="p158682156524"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p10868181515219"><a name="p10868181515219"></a><a name="p10868181515219"></a>否</p>
    </td>
    </tr>
    <tr id="row10869201595211"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p6868315185216"><a name="p6868315185216"></a><a name="p6868315185216"></a>SFS（弹性文件服务 ）节点存储大小</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p11869131525218"><a name="p11869131525218"></a><a name="p11869131525218"></a>40GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p11869161518520"><a name="p11869161518520"></a><a name="p11869161518520"></a>100GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p586991520526"><a name="p586991520526"></a><a name="p586991520526"></a>100GB</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p14869201545215"><a name="p14869201545215"></a><a name="p14869201545215"></a>500GB</p>
    </td>
    </tr>
    <tr id="row38503225544"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1785182211542"><a name="p1785182211542"></a><a name="p1785182211542"></a>EIP（弹性公网IP）</p>
    </td>
    <td class="cellrowborder" colspan="4" valign="top" headers="mcps1.2.6.1.2 mcps1.2.6.1.3 mcps1.2.6.1.4 mcps1.2.6.1.5 "><p id="p985113226544"><a name="p985113226544"></a><a name="p985113226544"></a>类型：全动态BGP；带宽： 5 Mbit/s</p>
    </td>
    </tr>
    </tbody>
    </table>

4.  单击“下一步：资源配置”，进行资源配置，参数如[表3](#table169417818359)所示。

    **表 3**  资源配置

    <a name="table169417818359"></a>
    <table><thead align="left"><tr id="row6942083350"><th class="cellrowborder" valign="top" width="21.92%" id="mcps1.2.4.1.1"><p id="p1394258113517"><a name="p1394258113517"></a><a name="p1394258113517"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.080000000000005%" id="mcps1.2.4.1.2"><p id="p79423813512"><a name="p79423813512"></a><a name="p79423813512"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.4.1.3"><p id="p99441488357"><a name="p99441488357"></a><a name="p99441488357"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row99442883515"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p8531453429"><a name="p8531453429"></a><a name="p8531453429"></a>环境资源</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p64411217116"><a name="p64411217116"></a><a name="p64411217116"></a>根据实际需求选择“创建默认环境”或“自定义环境”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p185273513427"><a name="p185273513427"></a><a name="p185273513427"></a>自定义环境</p>
    </td>
    </tr>
    <tr id="row12452183234410"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p944593419428"><a name="p944593419428"></a><a name="p944593419428"></a>集群</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p52911010904"><a name="p52911010904"></a><a name="p52911010904"></a>用于部署区块链服务。</p>
    <p id="p94451334104214"><a name="p94451334104214"></a><a name="p94451334104214"></a>可以使用已有CCE集群，创建新的CCE集群或者使用边缘集群。如果选择边缘集群，需要先纳管边缘节点并检查边缘节点状态。</p>
    <div class="note" id="note064741261420"><a name="note064741261420"></a><a name="note064741261420"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul241819586461"></a><a name="ul241819586461"></a><ul id="ul241819586461"><li>使用已有集群支持CCE 1.15及以下版本，还支持CCE 1.19版本。</li><li>Fabric1.4版本服务仅支持CCE 1.15及以下版本集群。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p16445734184212"><a name="p16445734184212"></a><a name="p16445734184212"></a>创建新的CCE集群</p>
    </td>
    </tr>
    <tr id="row16452113216447"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p444593474211"><a name="p444593474211"></a><a name="p444593474211"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p164452342429"><a name="p164452342429"></a><a name="p164452342429"></a>选择云主机所在的可用区。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p1445143413421"><a name="p1445143413421"></a><a name="p1445143413421"></a>可用区1</p>
    </td>
    </tr>
    <tr id="row545253214413"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p6445103419427"><a name="p6445103419427"></a><a name="p6445103419427"></a>云主机规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p114452034174219"><a name="p114452034174219"></a><a name="p114452034174219"></a>选择CCE集群中云主机的规格。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p9445123454212"><a name="p9445123454212"></a><a name="p9445123454212"></a>4核/8GB</p>
    </td>
    </tr>
    <tr id="row1945283294412"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p10446203419422"><a name="p10446203419422"></a><a name="p10446203419422"></a>云主机个数</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p238418107137"><a name="p238418107137"></a><a name="p238418107137"></a>根据实际需求输入云主机个数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p0446134204214"><a name="p0446134204214"></a><a name="p0446134204214"></a>2</p>
    </td>
    </tr>
    <tr id="row445213244419"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p5446534114213"><a name="p5446534114213"></a><a name="p5446534114213"></a>高可用</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p12446163434214"><a name="p12446163434214"></a><a name="p12446163434214"></a>若您对系统可靠性要求比较高，可购买高可用云主机。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p844623413428"><a name="p844623413428"></a><a name="p844623413428"></a>否</p>
    </td>
    </tr>
    <tr id="row1345283212449"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p114461634194211"><a name="p114461634194211"></a><a name="p114461634194211"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p3446113414421"><a name="p3446113414421"></a><a name="p3446113414421"></a>支持创建虚拟私有云、系统自动创建VPC和选择已有虚拟私有云。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p1446113464211"><a name="p1446113464211"></a><a name="p1446113464211"></a>系统自动创建VPC</p>
    </td>
    </tr>
    <tr id="row132801111154512"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p52801211184517"><a name="p52801211184517"></a><a name="p52801211184517"></a>所在子网</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p0280161116456"><a name="p0280161116456"></a><a name="p0280161116456"></a>通过子网提供与其他网络隔离的、可以独享的网络资源，以提高网络安全。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p628031113453"><a name="p628031113453"></a><a name="p628031113453"></a>系统自动创建子网</p>
    </td>
    </tr>
    <tr id="row3451632104416"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p18446634194215"><a name="p18446634194215"></a><a name="p18446634194215"></a>云主机登录方式</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p139141911201414"><a name="p139141911201414"></a><a name="p139141911201414"></a>支持密码、密钥对两种方式。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p6446163454211"><a name="p6446163454211"></a><a name="p6446163454211"></a>密码</p>
    </td>
    </tr>
    <tr id="row14512032104416"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p12446123412421"><a name="p12446123412421"></a><a name="p12446123412421"></a>root密码</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p1444643411428"><a name="p1444643411428"></a><a name="p1444643411428"></a>登录云主机时的root用户密码。</p>
    <p id="p48131915678"><a name="p48131915678"></a><a name="p48131915678"></a>如果填写该项，则以填写值为准，如果不填写，则以资源初始密码为准。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p744683420423"><a name="p744683420423"></a><a name="p744683420423"></a>-</p>
    </td>
    </tr>
    <tr id="row1045193294417"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p7499201374617"><a name="p7499201374617"></a><a name="p7499201374617"></a>确认密码</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p1499161384617"><a name="p1499161384617"></a><a name="p1499161384617"></a>再次输入登录云主机时的root用户密码进行确认。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p17500131311463"><a name="p17500131311463"></a><a name="p17500131311463"></a>-</p>
    </td>
    </tr>
    <tr id="row31542102169"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p331310212187"><a name="p331310212187"></a><a name="p331310212187"></a>是否使用CCE集群节点弹性IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><a name="ul85511147122018"></a><a name="ul85511147122018"></a><ul id="ul85511147122018"><li>选择“是”，则将集群中绑定的弹性IP地址作为区块链网络访问地址，如果集群没有弹性IP，请先给集群绑定弹性IP后，再购买区块链服务；</li><li>选择“否”，则将使用集群内部地址作为区块链网络访问地址，应用需要和集群内部网络互通才能正常工作。</li></ul>
    <p id="p123149281814"><a name="p123149281814"></a><a name="p123149281814"></a>区块链服务支持EIP开启IPv6转换，开启后，将提供IPv4和IPv6弹性公网ip地址，区块链业务不受影响，如何开启请参见<a href="https://support.huaweicloud.com/bcs_faq/bcs_faq_1211.html" target="_blank" rel="noopener noreferrer">弹性IP如何开启IPv6转换功能</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p13141022187"><a name="p13141022187"></a><a name="p13141022187"></a>是</p>
    </td>
    </tr>
    <tr id="row1475213195147"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p931418213183"><a name="p931418213183"></a><a name="p931418213183"></a>弹性IP计费方式</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><a name="ul1131412215188"></a><a name="ul1131412215188"></a><ul id="ul1131412215188"><li>如果计费方式选择的是“包年包月”，则弹性IP计费方式为“按带宽计费”；</li><li>如果计费方式选择的是“按需计费”，则弹性IP计费方式可以选择为“按带宽计费”或者“按流量计费”。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p931415211819"><a name="p931415211819"></a><a name="p931415211819"></a>按带宽计费</p>
    </td>
    </tr>
    <tr id="row1745173214443"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p331522181819"><a name="p331522181819"></a><a name="p331522181819"></a>弹性IP带宽</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.080000000000005%" headers="mcps1.2.4.1.2 "><p id="p8315182121815"><a name="p8315182121815"></a><a name="p8315182121815"></a>根据实际需求，选择弹性IP带宽。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.3 "><p id="p73152261813"><a name="p73152261813"></a><a name="p73152261813"></a>5 Mbit/s</p>
    </td>
    </tr>
    </tbody>
    </table>

5.  单击“下一步：区块链配置”，进行区块链配置，参数如[表4](#table2088518231)所示。

    **表 4**  区块链配置

    <a name="table2088518231"></a>
    <table><thead align="left"><tr id="row18925110231"><th class="cellrowborder" valign="top" width="21.92%" id="mcps1.2.4.1.1"><p id="p169155122314"><a name="p169155122314"></a><a name="p169155122314"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.99%" id="mcps1.2.4.1.2"><p id="p17910511233"><a name="p17910511233"></a><a name="p17910511233"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.09%" id="mcps1.2.4.1.3"><p id="p29115113231"><a name="p29115113231"></a><a name="p29115113231"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row79135115236"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p1191651152318"><a name="p1191651152318"></a><a name="p1191651152318"></a>区块链配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p29175117239"><a name="p29175117239"></a><a name="p29175117239"></a>根据实际需求选择“系统默认配置”或“自定义配置”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p129195118236"><a name="p129195118236"></a><a name="p129195118236"></a>自定义配置</p>
    </td>
    </tr>
    <tr id="row11522155717260"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p13523145716261"><a name="p13523145716261"></a><a name="p13523145716261"></a>区块链管理初始密码</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p4523357122616"><a name="p4523357122616"></a><a name="p4523357122616"></a>输入登录区块链服务管理界面的admin账户的密码进行确认。</p>
    <p id="p35501221155913"><a name="p35501221155913"></a><a name="p35501221155913"></a>如果填写该项，则以填写值为准，如果不填写，则以资源初始密码为准。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p12523185719267"><a name="p12523185719267"></a><a name="p12523185719267"></a>-</p>
    </td>
    </tr>
    <tr id="row13332114511268"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p161201945122616"><a name="p161201945122616"></a><a name="p161201945122616"></a>区块链管理确认密码</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p31203456263"><a name="p31203456263"></a><a name="p31203456263"></a>再次输入登录区块链服务管理界面的admin账户的密码进行确认。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p1412014451266"><a name="p1412014451266"></a><a name="p1412014451266"></a>-</p>
    </td>
    </tr>
    <tr id="row16327645102619"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p101210455263"><a name="p101210455263"></a><a name="p101210455263"></a>存储卷类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><a name="ul19121104519265"></a><a name="ul19121104519265"></a><ul id="ul19121104519265"><li>文件存储卷：高带宽、大容量的文件存储服务。</li><li>极速文件存储卷：低时延、高IOPS的文件存储服务。<p id="p1012119455263"><a name="p1012119455263"></a><a name="p1012119455263"></a>极速文件存储卷（SFS Turbo）备份与数据恢复功能使用，请参见<a href="https://support.huaweicloud.com/bcs_faq/bcs_faq_0909.html" target="_blank" rel="noopener noreferrer">极速文件存储卷（SFS Turbo）备份与数据恢复功能使用指导</a>。</p>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p11231445122619"><a name="p11231445122619"></a><a name="p11231445122619"></a>极速文件存储卷</p>
    </td>
    </tr>
    <tr id="row04518196277"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p1642785114240"><a name="p1642785114240"></a><a name="p1642785114240"></a>节点组织存储容量</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p3427165102413"><a name="p3427165102413"></a><a name="p3427165102413"></a>用于存储共享分布式账本，共识数据和中间结果等。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p64272519246"><a name="p64272519246"></a><a name="p64272519246"></a>500GB</p>
    </td>
    </tr>
    <tr id="row2370162520273"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p1080392612272"><a name="p1080392612272"></a><a name="p1080392612272"></a>账本数据存储方式</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p080312265277"><a name="p080312265277"></a><a name="p080312265277"></a>支持多种存储方式，不同方式的区别可参见界面提示信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p178031926132713"><a name="p178031926132713"></a><a name="p178031926132713"></a>文件数据库（GoLevelDB）</p>
    </td>
    </tr>
    <tr id="row114210347384"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p543534183820"><a name="p543534183820"></a><a name="p543534183820"></a>部署方式</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p155861324144010"><a name="p155861324144010"></a><a name="p155861324144010"></a>当版本类型选择“铂金版”时需要设置该参数。</p>
    <a name="ul38021636103915"></a><a name="ul38021636103915"></a><ul id="ul38021636103915"><li>选择“全量部署”，则在购买区块链服务时需将全部Peer节点配置到节点组织中。</li><li>选择“部分部署”，则在购买区块链服务时只需将部分Peer节点配置到节点组织中，剩余Peer节点可在购买区块链服务以后任意时刻通过添加组织或添加节点方式部署。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p14320344389"><a name="p14320344389"></a><a name="p14320344389"></a>部分部署</p>
    </td>
    </tr>
    <tr id="row18317194517267"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p12125164552612"><a name="p12125164552612"></a><a name="p12125164552612"></a>peer节点组织</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p1212574582616"><a name="p1212574582616"></a><a name="p1212574582616"></a>为区块链服务添加peer节点组织。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p1312584518263"><a name="p1312584518263"></a><a name="p1312584518263"></a>organization，节点数量为2。</p>
    </td>
    </tr>
    <tr id="row54757784219"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p14763784214"><a name="p14763784214"></a><a name="p14763784214"></a>部署节点总数</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p17476117174219"><a name="p17476117174219"></a><a name="p17476117174219"></a>当版本类型选择“铂金版”且部署方式为“部分部署”时，需要设置该参数。最大可设置为铂金版Peer节点配额。</p>
    <div class="note" id="note1781114219593"><a name="note1781114219593"></a><a name="note1781114219593"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p175779429597"><a name="p175779429597"></a><a name="p175779429597"></a>所有Peer节点自购买区块链订单完成之后开始计费。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p2476187184215"><a name="p2476187184215"></a><a name="p2476187184215"></a>50</p>
    </td>
    </tr>
    <tr id="row12466425173413"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p1612716458269"><a name="p1612716458269"></a><a name="p1612716458269"></a>通道配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p131272045132615"><a name="p131272045132615"></a><a name="p131272045132615"></a>通道主要用于实现联盟链中业务的隔离。通道内包含业务的参与方（联盟内的部分或全部组织）作为通道成员。每个通道可视为一条子链，并且对应一套分布式账本。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p1612717459268"><a name="p1612717459268"></a><a name="p1612717459268"></a>默认创建名为“channel”的实例通道，并将刚才创建的示例节点组织添加进此通道。</p>
    </td>
    </tr>
    <tr id="row9408192195911"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p2040892116598"><a name="p2040892116598"></a><a name="p2040892116598"></a>共识节点数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p1457111237147"><a name="p1457111237147"></a><a name="p1457111237147"></a>区块链网络中参与交易共识的节点数量。</p>
    <p id="p17571152312143"><a name="p17571152312143"></a><a name="p17571152312143"></a>当共识策略是Raft(CFT)时，共识节点数量为3。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p1457102371411"><a name="p1457102371411"></a><a name="p1457102371411"></a>3</p>
    </td>
    </tr>
    <tr id="row13308194512620"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p81261945152618"><a name="p81261945152618"></a><a name="p81261945152618"></a>安全机制</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p14126845172610"><a name="p14126845172610"></a><a name="p14126845172610"></a>保证数据安全的加密算法，支持ECDSA和国密算法。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p1126845122612"><a name="p1126845122612"></a><a name="p1126845122612"></a>ECDSA</p>
    </td>
    </tr>
    <tr id="row172951345182616"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p17128945192617"><a name="p17128945192617"></a><a name="p17128945192617"></a>区块生成配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p12128174512261"><a name="p12128174512261"></a><a name="p12128174512261"></a>产生的区块配置可支持区块产生时间，区块交易数量和区块容量，其中任何一个条件满足，区块就会产生，可根据交易频率和业务量灵活配置。</p>
    <p id="p2501123811202"><a name="p2501123811202"></a><a name="p2501123811202"></a>请根据实际选择<span class="uicontrol" id="uicontrol134188494209"><a name="uicontrol134188494209"></a><a name="uicontrol134188494209"></a>“是”</span>或<span class="uicontrol" id="uicontrol741894913204"><a name="uicontrol741894913204"></a><a name="uicontrol741894913204"></a>“否”</span>：</p>
    <a name="ul1540411352212"></a><a name="ul1540411352212"></a><ul id="ul1540411352212"><li>是：自定义设置以下参数：区块产生时间、区块交易数量和区块容量。</li><li>否：无需设置参数，区块产生时间默认为2秒、区块交易数量默认为500个和区块容量默为2MB。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p11128114512267"><a name="p11128114512267"></a><a name="p11128114512267"></a>否</p>
    </td>
    </tr>
    <tr id="row33451221522"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p512774519263"><a name="p512774519263"></a><a name="p512774519263"></a>添加RESTful API支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p101284456269"><a name="p101284456269"></a><a name="p101284456269"></a>若您需要使用RESTful方式进行链代码调用，则选择“是”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p1812844519264"><a name="p1812844519264"></a><a name="p1812844519264"></a>否</p>
    </td>
    </tr>
    <tr id="row12861245102612"><td class="cellrowborder" valign="top" width="21.92%" headers="mcps1.2.4.1.1 "><p id="p5129545182610"><a name="p5129545182610"></a><a name="p5129545182610"></a>添加可信计算平台</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.99%" headers="mcps1.2.4.1.2 "><p id="p1927193316221"><a name="p1927193316221"></a><a name="p1927193316221"></a>基于区块链，结合可信执行环境TEE（Trusted Execution Environment）实现数据资产可信共享，多方数据安全计算，保障数据隐私，达到数据可用不可见，实现全流程可信。</p>
    <p id="p8129114516267"><a name="p8129114516267"></a><a name="p8129114516267"></a>以下特点的区块链服务暂不支持：基础版服务、边缘集群、国密算法。</p>
    <p id="p131291045172619"><a name="p131291045172619"></a><a name="p131291045172619"></a>请根据实际选择<span class="uicontrol" id="uicontrol17130445162613"><a name="uicontrol17130445162613"></a><a name="uicontrol17130445162613"></a>“是”</span>或<span class="uicontrol" id="uicontrol913054532617"><a name="uicontrol913054532617"></a><a name="uicontrol913054532617"></a>“否”</span>：</p>
    <a name="ul713010454263"></a><a name="ul713010454263"></a><ul id="ul713010454263"><li>是：表示添加可信计算平台，可信计算平台的详细信息请参见<a href="可信计算平台（公测）.md">可信计算平台（公测）</a>。</li><li>否：表示不添加可信计算平台，若您后期需要添加可信计算平台，请参见<a href="插件介绍.md">插件介绍</a>安装可信插件。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.4.1.3 "><p id="p17131144517261"><a name="p17131144517261"></a><a name="p17131144517261"></a>否</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“下一步：确认订单”。
7.  确认配置信息无误后，勾选协议和免责声明，并单击“提交订单”。

    请等待数分钟，安装页面提示安装成功，查看服务状态变为“正常”后，表示区块链服务部署完成。

    ![](figures/zh-cn_image_0000001171927971.png)


## 后续操作（可选）<a name="section9233233314"></a>

已部署的服务，支持查看创建、删除、升级、添加组织、添加节点操作记录。左侧操作状态栏会展示已有操作记录的状态，操作状态类型包括：进行中、成功和失败。

![](figures/zh-cn_image_0000001083008746.png)

系统将保留最近三天的操作记录。

1.  登录区块链服务管理控制台，单击左侧导航栏中的“服务管理”。
2.  单击“操作记录”，查看各个资源的操作记录。

    您可以按资源名称关键词搜索操作记录，还可以在资源所在行进行“操作详情”及“删除”操作。


部署BCS的集群节点支持增加反亲和标签，在您需要将应用部署到区块链集群中时作区分隔离，以保证系统正常工作。

1.  登录CCE控制台，选择“资源管理 \> 节点管理”，可以看到节点列表，单击“操作”栏的“标签管理”。
2.  单击“添加标签”，填写需要增加标签的“键”为“nodeScope”、“值”为“userApplication”。
3.  单击“确定”，可以看到“标签变更成功”，再次单击“标签管理”，可查看到已经添加的标签。

