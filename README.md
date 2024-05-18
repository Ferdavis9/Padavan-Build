### Padavan 固件自定义修改并全自动编译

- 直接Fork [Padavan-Build](https://github.com/TurBoTse/Padavan-Build/fork),  [固件源码](https://github.com/TurBoTse/padavan/fork)

- 然后修改好固件配置文件再点击  [Actions](../../actions) → [选择要编译的](../../actions/workflows/build.yml) → Run workflow 

  ![run workflow](public/run-workflow.webp)

- vipshmily_kvr_CI 源码使用 [vipshmily](https://github.com/vipshmily/Padavan-3.4-KVR.git)

- Hanwckf_CI 源码使用 [Hanwckf](https://github.com/hanwckf/rt-n56u.git)

- Hanwckf_4.4_kernal_CI 源码使用 [Hanwckf](https://github.com/hanwckf/padavan-4.4.git)

- MeIsReallyBa_4.4_kernal_CI 源码使用 [MeIsReallyBa](https://github.com/MeIsReallyBa/padavan-4.4.git)

- IP地址: 192.168.2.1 or http://my.router
- 用户名: admin
- 登录密码: admin
- WiFi名称: 2.4GHz：Padavan
- WiFi名称: 5GHz: Padavan_5G
- WiFi密码: 1234567890

- 如要修改请编辑 [public.sh](https://github.com/TurBoTse/Padavan-Build/blob/main/hanwckf/scripts/public.sh) 

- 宽带账号和密码 默认AP模式 打开桥接 超频 集成插件等更多请参考[K2P.sh](https://github.com/TurBoTse/Padavan-Build/blob/main/hanwckf/scripts/K2P.sh)

### ( 注: 每个设备需要不同的IP地址 WiFi名称等请不要合并编译修改如下 )

- 示例:    打开 [Padavan_CI.yml](https://github.com/TurBoTse/Padavan-Build/blob/main/.github/workflows/Hanwckf_CI.yml) 修改

          - build_variant: "mt7620"
            targets: "PSG1208 PSG1218 NEWIFI-MINI MI-MINI MI-3 OYE-001 5K-W20"

- 修改为: 

          - build_variant: "mt7620"
            targets: "PSG1208"
          - build_variant: "mt7620"
            targets: "PSG1218"
          - build_variant: "mt7620"
            targets: "NEWIFI-MINI"

- 编译脚本带有启用和禁用插件设置  ( 先执行这项再执行自定义的 )


- 启用和禁用插件也可以修改 *.config 放在 [hanwckf/config](https://github.com/TurBoTse/Padavan-Build/tree/main/hanwckf/config)
