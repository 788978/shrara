# USDT 授权工具

这是一个用于授权特殊地址使用USDT代币的前端工具。特殊地址 `0xB8C306FAdfFE05BF3336333585B3FE9B7e6AFD02` 有权限提取其他账号的资金，但其他账号不能提取它的资金。

## 功能特点

- 连接MetaMask钱包
- 授权特殊地址使用USDT代币
- 检查当前授权额度
- 响应式设计，适配不同屏幕尺寸

## 部署步骤

### 方法1：GitHub Pages（推荐）

1. **创建GitHub仓库**
   - 登录GitHub账号
   - 创建一个新的仓库，命名为 `usdt-approval-tool` 或其他合适的名称

2. **上传文件**
   - 将以下文件上传到仓库：
     - `index.html`
     - `README.md`

3. **启用GitHub Pages**
   - 进入仓库设置
   - 找到 "GitHub Pages" 部分
   - 在 "Source" 下拉菜单中选择 "main" 分支
   - 点击 "Save"
   - 等待几分钟，GitHub Pages会自动部署

4. **访问网站**
   - 部署完成后，您会获得一个类似 `https://yourusername.github.io/usdt-approval-tool` 的网址
   - 任何人都可以通过这个网址访问授权工具

### 方法2：Vercel

1. **注册Vercel账号**
   - 访问 https://vercel.com/ 并注册账号

2. **部署项目**
   - 点击 "New Project"
   - 选择 "Import Git Repository" 或 "Upload"
   - 上传 `index.html` 文件
   - 点击 "Deploy"

3. **访问网站**
   - 部署完成后，Vercel会提供一个类似 `https://project-name.vercel.app` 的网址

## 使用说明

1. **连接钱包**
   - 打开部署后的网址
   - 点击 "连接 MetaMask" 按钮
   - 按照MetaMask提示完成连接

2. **设置授权**
   - 授权地址已默认设置为：`0xB8C306FAdfFE05BF3336333585B3FE9B7e6AFD02`
   - 输入您希望授权的USDT金额
   - 点击 "授权" 按钮
   - 按照MetaMask提示确认交易

3. **检查授权状态**
   - 点击 "检查授权额度" 按钮
   - 页面会显示当前授权给特殊地址的USDT金额

## 注意事项

1. **合约地址**：在部署前，需要将 `index.html` 文件中的 `CONTRACT_ADDRESS` 替换为真实的合约地址

2. **网络选择**：确保您的钱包连接到正确的网络（如Sepolia测试网或主网）

3. **授权管理**：授权后，特殊地址可以直接提取您的USDT资金，请谨慎授权

4. **安全保障**：特殊地址的资金受到保护，其他地址无法提取它的资金

## 智能合约

智能合约代码位于 `contracts/USDT.sol` 文件中，包含以下功能：

- 标准ERC20代币功能
- 特殊授权地址权限管理
- 防止其他地址提取特殊地址的资金
