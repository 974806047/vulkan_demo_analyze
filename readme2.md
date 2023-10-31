建议使用merge工具查看当前文件同上一个的区别

当前代码包含的顶点缓冲区到纹理映射章节的代码

谈论的主题
* 高速显存
* 如何向显卡传递顶点数据
* 如何向显卡传递全局信息
  * 传递矩阵或者向量
  * 传递图片
* Barrier

```
VkDescriptorSetLayout descriptorSetLayout;
VkImage textureImage;
VkDeviceMemory textureImageMemory;
VkImageView textureImageView;
VkSampler textureSampler;

VkBuffer vertexBuffer;
VkDeviceMemory vertexBufferMemory;
VkBuffer indexBuffer;
VkDeviceMemory indexBufferMemory;

std::vector<VkBuffer> uniformBuffers;
std::vector<VkDeviceMemory> uniformBuffersMemory;
std::vector<void*> uniformBuffersMapped;

VkDescriptorPool descriptorPool;
std::vector<VkDescriptorSet> descriptorSets;
```
```
void initVulkan() {
    createInstance();
    setupDebugMessenger();
    createSurface();
    pickPhysicalDevice();
    createLogicalDevice();
    createSwapChain();
    createImageViews();
    createRenderPass();
    createDescriptorSetLayout(); //
    createGraphicsPipeline();
    createFramebuffers();
    createCommandPool();
    createTextureImage(); //
    createTextureImageView(); //
    createTextureSampler(); //
    createVertexBuffer(); //
    createIndexBuffer(); //
    createUniformBuffers(); //
    createDescriptorPool(); //
    createDescriptorSets(); //
    createCommandBuffers();
    createSyncObjects();
}

```