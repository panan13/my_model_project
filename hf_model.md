# 一、平台做介绍以及一些拓展知识
以下是对 Hugging Face、ModelScope（魔搭社区）和 Modelers（魔乐社区）这三个AI学习社区的特点及操作的总结：
### **Hugging Face**
1. **简介**：
   - Hugging Face 是一个机器学习社区，提供超过 100,000 个预训练模型和 10,000 个数据集，是机器学习界的重要工具。
   - 适合模型下载、上传，以及快速构建和部署 web 应用（Spaces 功能）。

2. **特点**：
   - 强大的 Transformers 库支持预训练模型的推理和迁移学习。
   - 社区活跃，丰富的文档和教程。
   - 提供 Hugging Face Spaces 功能，简化模型应用的部署。

3. **常用操作**：
   - 模型下载：支持通过 Python 脚本或 CLI 下载模型。
   - 模型上传：通过 CLI 结合 Git LFS 上传大文件。
   - 创建 Spaces：支持快速部署基于 HTML 的 web 应用。
### **ModelScope（魔搭社区）**
1. **简介**：
   - 由阿里达摩院推出的“模型即服务”平台，支持探索、推理、微调和部署 AI 模型。
   - 提供开发机功能，可直接在云端运行代码。

2. **特点**：
   - 提供免费 GPU/CPU 开发环境。
   - 集成 ModelScope 的 CLI 和 Python SDK，方便开发和部署。
   - 对社区模型有审核机制，确保质量。

3. **常用操作**：
   - 下载指定文件：通过 CLI 工具下载特定模型文件。
   - 上传模型：通过 web 界面或 Git 工具上传模型。
### **Modelers（魔乐社区）**
1. **简介**：
   - 提供多样化、开源模型的平台，注重协作和开源精神。
   - 支持最新深度学习工具，如 OpenMind Library。

2. **特点**：
   - 支持多种深度学习框架（如 PyTorch、MindSpore）。
   - 提供 OpenMind Library，原生支持昇腾 NPU，拓展性强。
   - 强调开发者间的模型协作和共享。

3. **常用操作**：
   - 下载模型：支持 Git LFS 和 OpenMind Library API。
   - 上传模型：通过 OpenMind 的 API 或 Git 推送模型到社区。
### **平台对比总结**

| 功能/平台        | Hugging Face                  | ModelScope（魔搭社区）          | Modelers（魔乐社区）         |
|------------------|-------------------------------|---------------------------------|-----------------------------|
| **注册门槛**    | 简单             | 国内用户友好     | 国内用户友好 |
| **核心功能**    | 模型库、Transformers、Spaces   | 模型库、免费开发机             | 模型库、OpenMind Library    |
| **开发工具**    | Python API、CLI               | CLI、Python SDK                | OpenMind Library、Git       |
| **上传模式**    | CLI + Git LFS                | Web 上传、Git 上传             | Git 上传、OpenMind API      |
| **适用人群**    | 海外用户、社区活跃开发者       | 国内开发者、企业               | 国内研究者、开源爱好者     |

### **GitHub Codespaces**

1. **简介**：
   - GitHub 提供的基于云的开发环境，集成 VS Code 的在线编辑器和运行环境。
   - 支持快速创建和使用开发环境，减少本地配置的复杂性。

2. **特点**：
   - **即开即用**：预装常用工具和库（如 Python、Node.js 等），支持快速启动开发环境。
   - **云端计算资源**：提供在线运行代码和调试的能力。
   - **与 GitHub 集成**：直接与 GitHub 仓库交互，无需额外配置。
   - **支持自定义环境**：通过配置 `.devcontainer` 文件自定义开发环境。

3. **常用操作**：

   #### 3.1 **创建 Codespace**：
   - 登录 GitHub，进入目标项目页面。
   - 点击 **Code** 按钮，选择 **Codespaces**，然后点击 **Create codespace on main**。

   #### 3.2 **使用 Codespace**：
   - 在在线 VS Code 编辑器中，可以直接编辑、运行代码。
   - 提供终端支持，便于安装依赖和运行脚本。
   - 可以选择不同模板（如 Jupyter Notebook）搭建数据科学或机器学习的环境。

   #### 3.3 **配置环境依赖**：
   - 在 Codespace 的终端中安装所需库，例如 Hugging Face 的 `transformers`：
     ```bash
     pip install transformers==4.38
     pip install accelerate==0.33.0
     ```

   #### 3.4 **保存和恢复工作环境**：
   - 所有更改都会实时保存到 GitHub 仓库。
   - 可随时重新启动 Codespace，恢复工作状态。

4. **适用场景**：
   - 对于临时性开发需求（如验证 Hugging Face 模型）。
   - 无法本地配置复杂环境时（如需要 GPU 的模型运行环境）。
   - 协作开发项目，多个开发者可以共享同一环境。

5. **优劣势**：

   | 优势                                      | 劣势                                    |
   |-----------------------------------------|---------------------------------------|
   | 减少本地环境配置的复杂性                  | 需要网络支持                           |
   | 集成 VS Code，提供熟悉的开发体验          | 硬件资源有限（如较少的存储空间和无 GPU）|
   | 直接与 GitHub 仓库集成，便于代码管理       | 需订阅高级服务才能获得更大算力支持      |
## 任务：
| 任务 | 描述 | 时间 |
| --- | --- | --- |
| [模型下载](https://huggingface.co/internlm/internlm2-chat-1_8b) | 使用Hugging Face平台、魔搭社区平台（可选）和魔乐社区平台（可选）下载文档中提到的模型（至少需要下载config.json文件、model.safetensors.index.json文件），请在必要的步骤以及结果当中截图。 | 20min |
| 模型上传（可选） | 将我们下载好的config.json文件（也自行添加其他模型相关文件）上传到对应HF平台和魔搭社区平台，并截图。 | 10min |
| Space上传（可选） | 在HF平台上使用Spaces并把intern_cobuild部署成功，关键步骤截图。 | 10min |

## 任务一展示：![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/68d61eb9ec17445bb27fba8bfd73fce3.png)
## 任务二展示：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/63e02e0c12154865b5bcd82ad1f23cc0.png)![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/83aeca9a733344878d8f2ce42c821ad7.png)![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6995bf8c97164a8594987ed57a656c1e.png)![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3ad3ffa2258244ceb317a78c6283e9eb.png)
## 任务三展示：
修改index.html即可。
![](https://i-blog.csdnimg.cn/direct/75d552deecb14e55bb25ce9542125a68.png)











