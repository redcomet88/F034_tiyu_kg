# F034 vue+neo4j 体育知识图谱系统|体育文献知识图谱vue+flask知识图谱管理+d3.js可视化

> 完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从github来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775
> 

关注B站，有好处！
编号:  F034

## 视频

[video(video-hpqTyGok-1761374716898)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=781824533)(image-https://i-blog.csdnimg.cn/img_convert/85e88002b2cd04312601edd104846a1a.jpeg)(title-vue+neo4j 体育文献知识图谱 Python Flask框架)]

## 1 系统简介
系统简介：本系统是一个基于Vue+Flask+Neo4j构建的体育知识图谱系统，其核心功能围绕体育文献知识的展示、检索、分析和用户管理展开。主要包括：首页，用于展示系统概览和最新文献动态；文献检索模块，提供体育文献的检索功能，支持通过关键词模糊搜索和高级筛选；知识图谱可视化模块，通过D3.js实现知识图谱的直观展示，并支持节点的交互式浏览和关系查询；知识管理模块，允许管理员对知识图谱进行编辑、添加和删除操作，确保知识库的准确性和完整性；以及用户管理模块，包含登录、注册功能，以及个人信息修改（包括头像和密码）的设置，确保系统的安全性和个性化体验。
## 2 功能设计
该系统采用前后端分离的架构模式，前端基于Vue.js生态系统，使用HTML、CSS、JavaScript以及Vue Router（用于路由导航）和D3.js（用于知识图谱可视化）等技术构建用户界面。前端通过API请求与Flask后端进行数据交互，Flask后端负责业务逻辑处理，并与Neo4j数据库（用于存储知识图谱）和MySQL数据库（用于存储用户数据和文献信息）进行交互。系统还包含一个爬虫模块，用于从外部体育文献来源抓取数据，并将其处理后存储到Neo4j和MySQL数据库中，为知识图谱的构建和文献检索提供数据支撑。此外，系统支持模糊检索功能，用户可以通过输入关键词进行智能搜索，并通过可视化界面直观了解相关知识点的关联关系。
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1d4d939b1446425e80bd4ee07ee9061f.jpeg)
### 2.2 功能模块图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f576ba05ee864b78b9939c99e5f35278.jpeg)
## 3 功能展示
### 3.1 登录 & 注册
登录注册做的是一个可以切换的登录注册界面，点击去登录后者去注册可以切换，背景是一个视频，循环播放。
登录需要验证用户名和密码是否正确，如果**不正确会有错误提示**。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c638da1650f640108529ba0b568f99aa.png)
注册需要**验证用户名是否存在**，如果错误会有提示。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d2625d00376f45cd923aade5373af504.png)
### 3.2 主页
主页的布局采用了左侧是菜单，右侧是操作面板的布局方法，右侧的上方还有用户的头像和退出按钮，如果是新注册用户，没有头像，这边则不显示，需要在个人设置中上传了头像之后就会显示。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5111b66adf794cdf9d11596f1ea37157.png)
最新知识图谱文献：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b17d8a5a71b44ffb885091ca515d06d8.png)
### 3.3 体育类文献的查询
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d9314f97f8d9411eb3dc85cc8d783cca.png)
### 3.4 知识图谱的构建
通过代码进行知识图谱的构建：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/805a352803bb4046a265913dc497e072.png)
neo4j自带的浏览器中的查看：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/82252e2cccf54e9a8ef95f786ec5238f.png)
### 3.5 知识图谱的可视化 + 查询
通过d3.js实现系统知识图谱的可视化：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4a795ce0c5f34b12a343d57a06ada353.png)
支持模糊查询：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d4a3dd887349437983d60b396978f464.png)
### 3.6 知识图谱的增删改查
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e79cdf516a274556b8f28c1e6389d3d6.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7aecc72a616348509829b4318a167a1f.png)
### 3.7 个人设置
个人设置方面包含了用户信息修改、密码修改功能。
用户信息修改中可以上传头像，完成用户的头像个性化设置，也可以修改用户其他信息。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4f6598f368bb44e988fccb658d8f902d.png)
修改密码需要输入用户旧密码和新密码，验证旧密码成功后，就可以完成密码修改。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/59e664d4251b433198a8ab3cf29d03ef.png)
## 4程序代码
### 4.1 代码说明
代码介绍：以下是一个使用D3.js实现体育知识图谱可视化的代码示例。该代码从Neo4j数据库中获取数据，并使用D3.js的力学布局将知识图谱可视化。节点表示体育相关实体，边表示它们之间的关系。
### 4.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1a9f09f6904a48379b5d5882b514ecea.png)

### 4.3 代码实例
```python
// 配置
const neo4jConfig = {
    uri: 'bolt://localhost:7687',
    user: 'neo4j',
    password: 'password'
};

// 使用Cypher查询获取节点和关系
const cypherQuery = `
    MATCH (n)-[r]->(m)
    RETURN id(n) as source, id(m) as target, type(r) as type
`;

// 创建图表容器
const width = 800;
const height = 600;
const svg = d3.select('body')
    .append('svg')
    .attr('width', width)
    .attr('height', height);

// 从Neo4j获取数据
async function fetchGraphData() {
    const driver = new neo4j.Driver(neo4jConfig.uri, neo4jConfig);
    const session = driver.session();
    
    try {
        const result = await session.run(cypherQuery);
        const nodes = [];
        const links = [];
        
        // 提取节点和关系
        result.records().forEach(record => {
            const source = record.get('source');
            const target = record.get('target');
            const type = record.get('type');
            links.push({ source, target, type });
            if (!nodes.find(n => n.id === source)) {
                nodes.push({ id: source });
            }
            if (!nodes.find(n => n.id === target)) {
                nodes.push({ id: target });
            }
        });
        
        return { nodes, links };
    } finally {
        await session.close();
        await driver.close();
    }
}

// 创建力学布局
async function createGraph() {
    const data = await fetchGraphData();
    
    const simulation = d3.forceSimulation()
        .force('link', d3.forceLink().id(d => d.id))
        .force('charge', d3.forceManyBody())
        .force('center', d3.forceCenter(width / 2, height / 2));

    const link = svg.append('g')
        .selectAll('line')
        .data(data.links)
        .enter()
        .append('line')
        .attr('stroke', '#999')
        .attr('stroke-width', 2);

    const node = svg.append('g')
        .selectAll('circle')
        .data(data.nodes)
        .enter()
        .append('circle')
        .attr('r', 10)
        .attr('fill', '#007bff')
        .call(d3.drag()
            .on('start', dragStarted)
            .on('drag', dragged)
            .on('end', dragEnded));

    simulation.nodes(data.nodes).on('tick', ticked);
    simulation.force('link').links(data.links);

    function ticked() {
        link.attr('x1', d => d.source.x)
            .attr('y1', d => d.source.y)
            .attr('x2', d => d.target.x)
            .attr('y2', d => d.target.y);

        node.attr('cx', d => d.x)
            .attr('cy', d => d.y);
    }

    function dragStarted(event) {
        if (!event.active) simulation.alphaTarget(0.3).restart();
        event.subject.fx = event.subject.x;
        event.subject.fy = event.subject.y;
    }

    function dragged(event) {
        event.subject.fx = event.x;
        event.subject.fy = event.y;
    }

    function dragEnded(event) {
        if (!event.active) simulation.alphaTarget(0);
        event.subject.fx = null;
        event.subject.fy = null;
    }
}

// 初始化图表
createGraph();
```
