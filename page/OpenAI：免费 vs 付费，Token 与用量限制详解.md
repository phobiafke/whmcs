# OpenAI：免费 vs 付费，Token 与用量限制详解

## OpenAI 使用额度与机器翻译额度无关

请注意，您在 Termsoup 因购买方案而附带的机器翻译额度（以字符计算），与 OpenAI 的使用额度（以 token 计算）完全无关。机器翻译额度目前可用于 Google、Microsoft 和 Amazon 三种翻译服务，而 OpenAI 的额度则需要您先注册 OpenAI 账号后方可使用。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

---

## OpenAI 免费试用：如何开始？

注册 OpenAI 账号并申请 API key 后，OpenAI 将免费提供价值 5 美元的 token 额度。点击左侧的 **Usage** 选项即可查看您的剩余额度。由于 OpenAI 用户众多，目前需要绑定信用卡信息才能正常使用（详见下方「OpenAI 付费使用」部分）。

![查看 OpenAI 使用额度](https://bbtdd.com/img/25077678204.webp)

---

## 什么是 Token？

传统机器翻译通常以字符数（character）计费，而 OpenAI 则以 **token** 计算用户使用 ChatGPT 的费用。根据 OpenAI 官方说明，token 的换算关系如下：

- 1 token ≈ 4 个英文字符  
- 1 token ≈ ¾ 个英文单词  
- 100 tokens ≈ 75 个英文单词  

计费详情请参考 OpenAI 的定价页面。

---

## OpenAI 付费使用：如何设置？

如果免费试用的 5 美元额度用完后，您可以通过付费方式继续使用 OpenAI 服务。具体操作如下：

1. 点击左侧的 **Billing** 选项。  
2. 选择 **Set up paid account**。  

![设置付费账户](https://bbtdd.com/img/01272623565283.webp)

3. 输入信用卡信息，然后点击 **Set up payment method**。  

![绑定信用卡](https://bbtdd.com/img/20128994688.webp)

完成上述步骤后，OpenAI 会从您的信用卡中扣除 5 美元作为授权验证费用。这笔费用是暂时性的，将在 7 天内自动退还。

通过 API 使用 ChatGPT 时，您的用量费用将直接从信用卡扣除，并支付给 OpenAI。

---

## 如何设定 OpenAI 用量限制？

通过 API key 使用 ChatGPT 是按需付费（Pay-as-you-go）的，系统会每月生成账单并从您的信用卡中扣除相应费用。如果您希望控制用量，可以按照以下步骤设置：

1. 点击左侧的 **Billing** 选项。  
2. 选择 **Usage limits**。  

在此，您可以为 OpenAI 用量设置两种限制：  

- **硬限制**：当用量达到设定金额时，服务将自动停止。  
- **软限制**：当用量接近设定金额时，系统会通过邮件通知您。  

例如，如果您希望每月用量不超过 50 美元（硬限制），可以设置当用量达到 45 美元时（软限制）收到通知。

![用量限制设置](https://bbtdd.com/img/14604951991859.webp)