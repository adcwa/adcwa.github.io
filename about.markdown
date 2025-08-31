
layout: page
title: About
permalink: /about/


<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: white; padding: 2rem; border-radius: 10px; margin-bottom: 2rem; text-align: center;">
  <h1 style="margin: 0 0 1rem 0; font-size: 2.5rem;">🎁 免费 AI 代理开发服务</h1>
  <p style="font-size: 1.2rem; margin: 0 0 1rem 0; font-weight: bold;"> 无开发费用！</p>
  <p style="font-size: 1rem; margin: 0;">让 AI 为您的业务场景提供智能化解决方案</p>
</div>

## 💰 您需要支付的成本

您只需要承担以下**实际运行成本**，直接支付给相应供应商：

- ☁️ **服务器成本** - 云服务器托管费用
- 🌐 **域名成本** - 如果需要自定义域名
- 🤖 **LLM API 成本** - OpenAI、Claude 等 AI 服务调用费用
- 🔧 **第三方服务成本** - 数据库、存储等附加服务

**开发、设计 - 完全免费！**

## 🤔 为什么免费？

我提供免费开发服务，是因为我希望：

- 🔍 **发现创新场景** - 寻找真正有变革性的 AI 应用场景
- 🚀 **验证技术价值** - 通过实际部署验证 AI 代理的商业价值
- 📈 **选择优质项目** - 从成功案例中选择几个有潜力的项目进行深度合作和分发
- 💡 **共创未来** - 与优秀的合作伙伴一起探索 AI 技术的无限可能

这不是简单的免费服务，而是一次共同探索 AI 未来的机会！

---

## 👨‍💻 关于我


<div style="text-align: center; margin: 0rem 0;">
  <svg width="600" height="300" viewBox="0 0 600 300" xmlns="http://www.w3.org/2000/svg">
    <!-- 背景 -->
    <defs>
      <linearGradient id="bgGradient" x1="0%" y1="0%" x2="100%" y2="100%">
        <stop offset="0%" style="stop-color:#667eea;stop-opacity:0.1" />
        <stop offset="100%" style="stop-color:#764ba2;stop-opacity:0.1" />
      </linearGradient>
      <linearGradient id="skillGradient" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" style="stop-color:#667eea" />
        <stop offset="100%" style="stop-color:#764ba2" />
      </linearGradient>
    </defs>
    
    <rect width="100%" height="100%" fill="url(#bgGradient)" rx="15"/>
    
    <!-- 中心AI核心 -->
    <circle cx="300" cy="150" r="40" fill="url(#skillGradient)" opacity="0.8">
      <animate attributeName="r" values="35;45;35" dur="3s" repeatCount="indefinite"/>
    </circle>
    <text x="300" y="150" text-anchor="middle" dominant-baseline="middle" fill="white" font-size="14" font-weight="bold">AI Core</text>
    
    <!-- 技能节点轮播 -->
    <g id="skills">
      <!-- LLM集成 -->
      <g class="skill-node" opacity="1">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="180" cy="150" r="25" fill="#FF6B6B" opacity="0.9">
          <animate attributeName="opacity" values="0.7;1;0.7" dur="2s" repeatCount="indefinite"/>
        </circle>
        <text x="180" y="145" text-anchor="middle" fill="white" font-size="10" font-weight="bold">LLM</text>
        <text x="180" y="155" text-anchor="middle" fill="white" font-size="8">Integration</text>
        <!-- 连接线 -->
        <line x1="220" y1="150" x2="260" y2="150" stroke="url(#skillGradient)" stroke-width="2" opacity="0.6">
          <animate attributeName="opacity" values="0.3;0.8;0.3" dur="1.5s" repeatCount="indefinite"/>
        </line>
      </g>
      
      <!-- 向量数据库 -->
      <g class="skill-node">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="420" cy="150" r="25" fill="#4ECDC4" opacity="0.9">
          <animate attributeName="opacity" values="0.7;1;0.7" dur="2.2s" repeatCount="indefinite"/>
        </circle>
        <text x="420" y="145" text-anchor="middle" fill="white" font-size="10" font-weight="bold">Vector</text>
        <text x="420" y="155" text-anchor="middle" fill="white" font-size="8">Database</text>
        <line x1="340" y1="150" x2="380" y2="150" stroke="url(#skillGradient)" stroke-width="2" opacity="0.6">
          <animate attributeName="opacity" values="0.3;0.8;0.3" dur="1.7s" repeatCount="indefinite"/>
        </line>
      </g>
      
      <!-- 框架技术 -->
      <g class="skill-node">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="300" cy="80" r="25" fill="#45B7D1" opacity="0.9">
          <animate attributeName="opacity" values="0.7;1;0.7" dur="1.8s" repeatCount="indefinite"/>
        </circle>
        <text x="300" y="75" text-anchor="middle" fill="white" font-size="9" font-weight="bold">LangChain</text>
        <text x="300" y="85" text-anchor="middle" fill="white" font-size="8">Framework</text>
        <line x1="300" y1="110" x2="300" y2="120" stroke="url(#skillGradient)" stroke-width="2" opacity="0.6">
          <animate attributeName="opacity" values="0.3;0.8;0.3" dur="1.4s" repeatCount="indefinite"/>
        </line>
      </g>
      
      <!-- 部署运维 -->
      <g class="skill-node">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="300" cy="220" r="25" fill="#96CEB4" opacity="0.9">
          <animate attributeName="opacity" values="0.7;1;0.7" dur="2.1s" repeatCount="indefinite"/>
        </circle>
        <text x="300" y="215" text-anchor="middle" fill="white" font-size="10" font-weight="bold">Cloud</text>
        <text x="300" y="225" text-anchor="middle" fill="white" font-size="8">Deploy</text>
        <line x1="300" y1="180" x2="300" y2="190" stroke="url(#skillGradient)" stroke-width="2" opacity="0.6">
          <animate attributeName="opacity" values="0.3;0.8;0.3" dur="1.6s" repeatCount="indefinite"/>
        </line>
      </g>
      
      <!-- 前端技术 -->
      <g class="skill-node">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="240" cy="100" r="20" fill="#FECA57" opacity="0.8">
          <animate attributeName="opacity" values="0.6;1;0.6" dur="1.9s" repeatCount="indefinite"/>
        </circle>
        <text x="240" y="95" text-anchor="middle" fill="white" font-size="8" font-weight="bold">React</text>
        <text x="240" y="105" text-anchor="middle" fill="white" font-size="7">Vue</text>
        <line x1="260" y1="120" x2="280" y2="135" stroke="url(#skillGradient)" stroke-width="1.5" opacity="0.5">
          <animate attributeName="opacity" values="0.2;0.7;0.2" dur="1.8s" repeatCount="indefinite"/>
        </line>
      </g>
      
      <!-- 后端技术 -->
      <g class="skill-node">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="360" cy="200" r="20" fill="#FF9FF3" opacity="0.8">
          <animate attributeName="opacity" values="0.6;1;0.6" dur="2.3s" repeatCount="indefinite"/>
        </circle>
        <text x="360" y="195" text-anchor="middle" fill="white" font-size="8" font-weight="bold">Python</text>
        <text x="360" y="205" text-anchor="middle" fill="white" font-size="7">FastAPI</text>
        <line x1="340" y1="180" x2="320" y2="165" stroke="url(#skillGradient)" stroke-width="1.5" opacity="0.5">
          <animate attributeName="opacity" values="0.2;0.7;0.2" dur="2.0s" repeatCount="indefinite"/>
        </line>
      </g>
      
      <!-- 监控运维 -->
      <g class="skill-node">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="150" cy="200" r="18" fill="#A8E6CF" opacity="0.8">
          <animate attributeName="opacity" values="0.6;1;0.6" dur="1.7s" repeatCount="indefinite"/>
        </circle>
        <text x="150" y="195" text-anchor="middle" fill="white" font-size="7" font-weight="bold">Monitor</text>
        <text x="150" y="205" text-anchor="middle" fill="white" font-size="6">Grafana</text>
        <line x1="170" y1="180" x2="280" y2="165" stroke="url(#skillGradient)" stroke-width="1.5" opacity="0.4">
          <animate attributeName="opacity" values="0.1;0.6;0.1" dur="2.2s" repeatCount="indefinite"/>
        </line>
      </g>
      
      <!-- API集成 -->
      <g class="skill-node">
        <animateTransform attributeName="transform" type="rotate" values="0 300 150;360 300 150" dur="20s" repeatCount="indefinite"/>
        <circle cx="450" cy="100" r="18" fill="#FFB4BA" opacity="0.8">
          <animate attributeName="opacity" values="0.6;1;0.6" dur="2.4s" repeatCount="indefinite"/>
        </circle>
        <text x="450" y="95" text-anchor="middle" fill="white" font-size="8" font-weight="bold">API</text>
        <text x="450" y="105" text-anchor="middle" fill="white" font-size="7">Gateway</text>
        <line x1="430" y1="120" x2="320" y2="135" stroke="url(#skillGradient)" stroke-width="1.5" opacity="0.4">
          <animate attributeName="opacity" values="0.1;0.6;0.1" dur="1.5s" repeatCount="indefinite"/>
        </line>
      </g>
    </g>
    
    <!-- 技能说明文字轮播 -->
    <g id="skill-text">
      <text x="300" y="270" text-anchor="middle" fill="#666" font-size="12" opacity="1">
        <animate attributeName="opacity" values="1;0;1" dur="4s" repeatCount="indefinite"/>
        全栈 AI 代理开发 • 从架构设计到生产部署
      </text>
    </g>
    
    <!-- 装饰性粒子 -->
    <g opacity="0.3">
      <circle cx="50" cy="50" r="2" fill="#667eea">
        <animate attributeName="cy" values="50;250;50" dur="8s" repeatCount="indefinite"/>
      </circle>
      <circle cx="550" cy="80" r="1.5" fill="#764ba2">
        <animate attributeName="cy" values="80;220;80" dur="6s" repeatCount="indefinite"/>
      </circle>
      <circle cx="80" cy="250" r="1" fill="#4ECDC4">
        <animate attributeName="cx" values="80;520;80" dur="10s" repeatCount="indefinite"/>
      </circle>
    </g>
  </svg>
</div>

**技术背景：**
- 🎯 10年+全栈开发经验，专注企业业务场景应用落地
- 🔥 精通 AI 代理架构设计和实现
- 🛠️ 熟练掌握多种 LLM 平台集成（OpenAI、Anthropic、Google 等）
- 🌐 全栈开发能力，从前端到后端一站式解决
- 📱 支持 Web、移动端、API 等多种部署方式

---

## 🚀 合作流程

1. **需求沟通** - 通过邮件详细讨论您的场景需求
2. **方案设计** - 提供技术方案
3. **原型开发** - 快速搭建 MVP 版本供您测试
4. **迭代优化** - 根据反馈持续改进
5. **部署上线** - 协助完成生产环境部署
6. **后续支持** - 提供必要的技术支持和维护指导

---
<!-- 
<div style="text-align: center; padding: 2rem; background: #e3f2fd; border-radius: 8px;">
  <h3 style="color: #1976d2; margin-top: 0;">💡 让我们一起打造您的专属 AI 代理！</h3>
  <p style="margin-bottom: 1rem;">无论是提升工作效率、改善客户体验，还是探索 AI 的创新应用</p>
  <a href="mailto:adcwangfeng@gmail.com?subject=AI代理开发需求咨询&body=🎯 用户场景编写模板%0A%0A请按照以下格式详细描述您的AI代理需求：%0A%0A## 1. 场景名称（Scenario Title）%0A简要描述这个场景的核心内容%0A示例：智能客服代理处理售后咨询%0A%0A您的场景：[请填写]%0A%0A----%0A%0A## 2. 用户画像（User Persona）%0A- 姓名：[请填写]%0A- 年龄：[请填写]%0A- 职业：[请填写]%0A- 使用设备/平台：[请填写，如：iPhone/Web浏览器/API接口]%0A- 技术水平：[请填写，如：熟练/一般/初学者]%0A- 主要目标：[请填写，用户希望通过AI代理实现什么]%0A%0A----%0A%0A## 3. 使用背景（Context of Use）%0A说明用户所处的时间、地点、环境等背景信息%0A%0A[请详细描述使用场景的背景，如：工作时间、在办公室、处理客户咨询等]%0A%0A----%0A%0A## 4. 期望功能（Expected Features）%0A详细描述您希望AI代理具备的功能%0A%0A[请列出具体功能需求，如：%0A- 自动回复常见问题%0A- 转接人工客服%0A- 记录客户信息%0A- 生成工作报告等]%0A%0A----%0A%0A## 5. 行为流程（User Actions）%0A描述用户与AI代理的交互流程%0A%0A步骤1：[用户操作] → [期望的AI反馈]%0A步骤2：[用户操作] → [期望的AI反馈]%0A步骤3：[用户操作] → [期望的AI反馈]%0A[可添加更多步骤]%0A%0A----%0A%0A## 6. 用户痛点与期望（Pain Points  Expectations）%0A%0A### 痛点：%0A[描述现有问题，如：%0A- 人工客服响应慢%0A- 重复性工作占用时间%0A- 信息查找效率低等]%0A%0A### 期望：%0A[描述期望的解决方案，如：%0A- 24小时快速响应%0A- 自动化处理常规任务%0A- 智能信息检索等]%0A%0A----%0A%0A## 7. 场景价值（Value of Scenario）%0A说明这个场景对您或业务的意义%0A%0A[请描述实现后的预期价值，如：提升客户满意度、节省人力成本、提高工作效率等]%0A%0A----%0A%0A## 8. 技术要求（Technical Requirements）%0A- 平台偏好：[Web/移动端/API/微信小程序/其他]%0A- 集成需求：[是否需要与现有系统集成，如CRM、数据库等]%0A- 性能要求：[响应时间、并发用户数等要求]%0A- 安全要求：[数据隐私、访问权限等要求]%0A%0A----%0A%0A## 9. 预算范围（Budget Range）%0A大概的月度运行成本预算 %0A%0A[请填写，如：100-500元/月、500-1000元/月等]%0A%0A----%0A%0A## 10. 时间要求（Timeline）%0A希望的项目完成时间%0A%0A[请填写，如：1个月内、2-3个月、无特殊要求等]%0A%0A----%0A%0A感谢您的详细描述！我会仔细分析您的需求并在24小时内回复技术方案和成本预估。" style="background: #1976d2; color: white; padding: 12px 24px; border-radius: 6px; text-decoration: none; font-weight: bold;">立即开始 →</a>
</div>
 -->
 

## 📧 开始合作


<div style="background: #f8f9fa; padding: 1.5rem; border-radius: 8px; border-left: 4px solid #28a745;">
  <h3 style="margin-top: 0; color: #28a745;">📮 联系我</h3>
  <p><strong>Email:</strong> <a href="mailto:adcwangfeng@gmail.com?subject=AI代理开发需求咨询&body=🎯 用户场景编写模板%0A%0A请按照以下格式详细描述您的AI代理需求：%0A%0A## 1. 场景名称（Scenario Title）%0A简要描述这个场景的核心内容%0A示例：智能客服代理处理售后咨询%0A%0A您的场景：[请填写]%0A%0A----%0A%0A## 2. 用户画像（User Persona）%0A- 姓名：[请填写]%0A- 年龄：[请填写]%0A- 职业：[请填写]%0A- 使用设备/平台：[请填写，如：iPhone/Web浏览器/API接口]%0A- 技术水平：[请填写，如：熟练/一般/初学者]%0A- 主要目标：[请填写，用户希望通过AI代理实现什么]%0A%0A----%0A%0A## 3. 使用背景（Context of Use）%0A说明用户所处的时间、地点、环境等背景信息%0A%0A[请详细描述使用场景的背景，如：工作时间、在办公室、处理客户咨询等]%0A%0A----%0A%0A## 4. 期望功能（Expected Features）%0A详细描述您希望AI代理具备的功能%0A%0A[请列出具体功能需求，如：%0A- 自动回复常见问题%0A- 转接人工客服%0A- 记录客户信息%0A- 生成工作报告等]%0A%0A----%0A%0A## 5. 行为流程（User Actions）%0A描述用户与AI代理的交互流程%0A%0A步骤1：[用户操作] → [期望的AI反馈]%0A步骤2：[用户操作] → [期望的AI反馈]%0A步骤3：[用户操作] → [期望的AI反馈]%0A[可添加更多步骤]%0A%0A----%0A%0A## 6. 用户痛点与期望（Pain Points  Expectations）%0A%0A### 痛点：%0A[描述现有问题，如：%0A- 人工客服响应慢%0A- 重复性工作占用时间%0A- 信息查找效率低等]%0A%0A### 期望：%0A[描述期望的解决方案，如：%0A- 24小时快速响应%0A- 自动化处理常规任务%0A- 智能信息检索等]%0A%0A----%0A%0A## 7. 场景价值（Value of Scenario）%0A说明这个场景对您或业务的意义%0A%0A[请描述实现后的预期价值，如：提升客户满意度、节省人力成本、提高工作效率等]%0A%0A----%0A%0A## 8. 技术要求（Technical Requirements）%0A- 平台偏好：[Web/移动端/API/微信小程序/其他]%0A- 集成需求：[是否需要与现有系统集成，如CRM、数据库等]%0A- 性能要求：[响应时间、并发用户数等要求]%0A- 安全要求：[数据隐私、访问权限等要求]%0A%0A----%0A%0A## 9. 预算范围（Budget Range）%0A大概的月度运行成本预算 %0A%0A[请填写，如：100-500元/月、500-1000元/月等]%0A%0A----%0A%0A## 10. 时间要求（Timeline）%0A希望的项目完成时间%0A%0A[请填写，如：1个月内、2-3个月、无特殊要求等]%0A%0A----%0A%0A感谢您的详细描述！我会仔细分析您的需求尽快回复技术方案。">adcwangfeng@gmail.com</a></p>
  <p><strong>邮件主题：</strong> AI代理开发需求咨询</p>
  <p><strong>模板说明：</strong> 点击邮箱链接会自动打开邮件，其中包含完整的需求描述模板</p>
  <p style="margin-bottom: 0;"><strong>响应时间：</strong> 视场景而定</p>
</div>
 