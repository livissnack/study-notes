# Laravel Homestead

- [介绍](#introduction)
- [安装与设置](#installation-and-setup)
    - [第一步](#first-steps)
    - [配置 Homestead](#configuring-homestead)
    - [启动 Vagrant Box](#launching-the-vagrant-box)
    - [根据项目安装](#per-project-installatio)
    - [安装 MariaDB](#installing-mariadb)
    - [安装 Elasticsearch](#installing-elasticsearch)
    - [别名](#aliases)
- [日常使用](#daily-usage)
    - [全局可用的 Homestead](#accessing-homestead-globally)
    - [通过 SSH 连接](#connecting-via-ssh)
    - [连接数据库](#connecting-to-databases)
    - [添加其他站点](#adding-additional-sites)
    - [环境变量](#environment-variables)
    - [配置 Cron 调度器](#configuring-cron-schedules)
    - [配置 Mailhog](#configuring-mailhog)
    - [端口](#ports)
    - [共享你的环境](#sharing-your-environment)
    - [多个 PHP 版本](#multiple-php-versions)
    - [Web 服务器](#web-servers)
- [网络接口](#network-interfaces)
- [更新 Homestead](#updating-homestead)
- [提供器的特殊设置](#provider-specific-settings)
    - [VirtualBox](#provider-specific-virtualbox)

<a name="introduction"></a>
## 简介

Laravel 致力于让整个 PHP 开发体验变得愉快， 包括你的本地开发环境。 [Vagrant](https://www.vagrantup.com) 提供了一种简单，优雅的方式来管理和配置虚拟机。

Laravel Homestead 是一个官方预封装的 Vagrant box，它为你提供了一个完美的开发环境，而无需在本地机器安装 PHP 、Web 服务器和其他服务器软件。不用担心会搞乱你的操作系统！Vagrant boxes 是一次性的。如果出现问题，你可以在几分钟内销毁并创建 Box!

Homestead 可以运行在任何 Windows，Mac，或 Linux 系统，它包括了 Nginx web 服务器， PHP 7.2，PHP 7.1，PHP 7.0，PHP 5.6， MySQL，PostgreSQL，Redis，Memcached， Node，以及开发 Laravel 应用程序所需要的东西。

> {note} 如果你使用 Windows，你可能需要通过 BIOS 来启用硬件虚拟化  (VT-x)。如果您在 UEFI 系统上使用 Hyper-V，可能还需要禁用 Hyper-V 才能访问 VT-x。

<a name="included-software"></a>
### 内置软件

<div class="content-list" markdown="1">
- Ubuntu 16.04
- Git
- PHP 7.2
- PHP 7.1
- PHP 7.0
- PHP 5.6
- Nginx
- Apache (Optional)
- MySQL
- MariaDB (Optional)
- Sqlite3
- PostgreSQL
- Composer
- Node (With Yarn, Bower, Grunt, and Gulp)
- Redis
- Memcached
- Beanstalkd
- Mailhog
- Elasticsearch (Optional)
- ngrok
</div>

<a name="installation-and-setup"></a>
## 安装与设置

<a name="first-steps"></a>
### 第一步

在启动 Homestead 环境之前，你必须安装 [VirtualBox 5.2](https://www.virtualbox.org/wiki/Downloads)， [VMWare](https://www.vmware.com)， [Parallels](https://www.parallels.com/products/desktop/) 或 [Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v) 以及 [Vagrant](https://www.vagrantup.com/downloads.html). 上述软件均针对不同操作系统提供了易于使用的可视化安装包。

若要使用 VMware 提供器，你需要购买 VMware Fusion / Workstation 和 [VMware Vagrant plug-in](https://www.vagrantup.com/vmware)。虽然它不是免费的，但 VMware 可以提供更快的共享文件夹性能。

若要使用 Parallels 提供器，你需要安装 [Parallels Vagrant plug-in](https://github.com/Parallels/vagrant-parallels). 这是免费的。

由于受到 [Vagrant 限制](https://www.vagrantup.com/docs/hyperv/limitations.html) ,  Hyper-V 提供程序会忽略所有网络设置。


