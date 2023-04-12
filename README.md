<div align="center">
<img src="./static/icon.svg" alt="预览"/>

<h1 align="center">ChatGPT Next Web</h1>


</div>

## 使用

1. 准备好你的 [OpenAI API Key](https://platform.openai.com/account/api-keys);
2. 点击右侧按钮开始部署：
   [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FYidadaa%2FChatGPT-Next-Web&env=OPENAI_API_KEY&env=CODE&project-name=chatgpt-next-web&repository-name=ChatGPT-Next-Web)，直接使用 Github 账号登陆即可，记得在环境变量页填入 API Key；
3. 部署完毕后，即可开始使用；
4. （可选）[绑定自定义域名](https://vercel.com/docs/concepts/projects/domains/add-a-domain)：Vercel 分配的域名 DNS 在某些区域被污染了，绑定自定义域名即可直连。

## Get Started

1. Get [OpenAI API Key](https://platform.openai.com/account/api-keys);
2. Click
   [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FYidadaa%2FChatGPT-Next-Web&env=OPENAI_API_KEY&env=CODE&project-name=chatgpt-next-web&repository-name=ChatGPT-Next-Web);
3. Enjoy :)

## 保持更新 Keep Updated

如果你按照上述步骤一键部署了自己的项目，可能会发现总是提示“存在更新”的问题，这是由于 Vercel 会默认为你创建一个新项目而不是 fork 本项目，这会导致无法正确地检测更新。
推荐你按照下列步骤重新部署：

- 删除掉原先的 repo；
- fork 本项目；
- 前往 vercel 控制台，删除掉原先的 project，然后新建 project，选择你刚刚 fork 出来的项目重新进行部署即可；
- 在重新部署的过程中，请手动添加名为 `OPENAI_API_KEY` 的环境变量，并填入你的 api key 作为值。

本项目会持续更新，如果你想让代码库总是保持更新，可以查看 [Github 的文档](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) 了解如何让 fork 的项目与上游代码同步，建议定期进行同步操作以获得新功能。

你可以 star/watch 本项目或者 follow 作者来及时获得新功能更新通知。

If you have deployed your own project with just one click following the steps above, you may encounter the issue of "Updates Available" constantly showing up. This is because Vercel will create a new project for you by default instead of forking this project, resulting in the inability to detect updates correctly.

We recommend that you follow the steps below to re-deploy:

- Delete the original repo;
- Fork this project;
- Go to the Vercel dashboard, delete the original project, then create a new project and select the project you just forked to redeploy;
- Please manually add an environment variable named `OPENAI_API_KEY` and enter your API key as the value during the redeploy process.

This project will be continuously maintained. If you want to keep the code repository up to date, you can check out the [Github documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) to learn how to synchronize a forked project with upstream code. It is recommended to perform synchronization operations regularly.

You can star or watch this project or follow author to get release notifictions in time.

## 配置密码 Password

本项目提供有限的权限控制功能，请在 Vercel 项目控制面板的环境变量页增加名为 `CODE` 的环境变量，值为用英文逗号分隔的自定义密码：

```
code1,code2,code3
```

增加或修改该环境变量后，请**重新部署**项目使改动生效。

This project provides limited access control. Please add an environment variable named `CODE` on the vercel environment variables page. The value should be passwords separated by comma like this:

```
code1,code2,code3
```

After adding or modifying this environment variable, please redeploy the project for the changes to take effect.

## 环境变量 Environment Variables

### `OPENAI_API_KEY` (required)

OpanAI 密钥。

Your openai api key.

### `CODE` (optional)

访问密码，可选，可以使用逗号隔开多个密码。

Access passsword, separated by comma.

### `BASE_URL` (optional)

> Default: `api.openai.com`

OpenAI 接口代理 URL。

Override openai api request base url.

### `PROTOCOL` (optional)

> Default: `https`

> Values: `http` | `https`

OpenAI 接口协议。

Override openai api request protocol.

## 开发 Development

点击下方按钮，开始二次开发：

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/Yidadaa/ChatGPT-Next-Web)

在开始写代码之前，需要在项目根目录新建一个 `.env.local` 文件，里面填入环境变量：

Before starting development, you must create a new `.env.local` file at project root, and place your api key into it:

```
OPENAI_API_KEY=<your api key here>
```

### 本地开发 Local Development

> 如果你是中国大陆用户，不建议在本地进行开发，除非你能够独立解决 OpenAI API 本地代理问题。

1. 安装 nodejs 和 yarn，具体细节请询问 ChatGPT；
2. 执行 `yarn install && yarn dev` 即可。

### 本地部署 Local Deployment

```shell
bash <(curl -s https://raw.githubusercontent.com/Yidadaa/ChatGPT-Next-Web/main/scripts/setup.sh)
```

### 容器部署 Docker Deployment

```shell
docker pull yidadaa/chatgpt-next-web

docker run -d -p 3000:3000 -e OPENAI_API_KEY="" -e CODE="" yidadaa/chatgpt-next-web
```

## 截图 Screenshots

![设置 Settings](./static/settings.png)

![更多展示 More](./static/more.png)


## 捐赠 Donate USDT
> BNB Smart Chain (BEP 20)
```
0x67cD02c7EB62641De576a1fA3EdB32eA0c3ffD89
```

## 鸣谢 Special Thanks

### 捐赠者 Sponsor

[@mushan0x0](https://github.com/mushan0x0)
[@ClarenceDan](https://github.com/ClarenceDan)
[@zhangjia](https://github.com/zhangjia)
[@hoochanlon](https://github.com/hoochanlon)

### 贡献者 Contributor

[Contributors](https://github.com/Yidadaa/ChatGPT-Next-Web/graphs/contributors)

## LICENSE

- [Anti 996 License](https://github.com/kattgu7/Anti-996-License/blob/master/LICENSE_CN_EN)
