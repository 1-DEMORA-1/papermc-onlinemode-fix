Paper [![Paper Build Status](https://img.shields.io/github/actions/workflow/status/PaperMC/Paper/build.yml?branch=master)](https://github.com/PaperMC/Paper/actions)
[![Discord](https://img.shields.io/discord/289587909051416579.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/papermc)
[![GitHub Sponsors](https://img.shields.io/github/sponsors/papermc?label=GitHub%20Sponsors)](https://github.com/sponsors/PaperMC)
[![Open Collective](https://img.shields.io/opencollective/all/papermc?label=OpenCollective%20Sponsors)](https://opencollective.com/papermc)
===========

## В этой версии paper (1.21) я сделал удобную адаптацию под пиратские сервера.
## Всё просто, при- запуске сервера в файле server.-properties параметр online-mode
## автоматически стоит на false.

## Скомпелированный jar файл вы можете скачать 

```0From 0000000000000000000000000000000000000000 Mon Sep 17 00:00:00 2001
From: Paper Developer <paper@papermc.io>
Date: $(date)
Subject: [PATCH] Set online-mode default to false

Changes the default value of online-mode in server.properties from true to false
for easier offline development and testing.

diff --git a/src/main/java/net/minecraft/server/dedicated/DedicatedServerProperties.java b/src/main/java/net/minecraft/server/dedicated/DedicatedServerProperties.java
index xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx..yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy 100644
--- a/src/main/java/net/minecraft/server/dedicated/DedicatedServerProperties.java
+++ b/src/main/java/net/minecraft/server/dedicated/DedicatedServerProperties.java
@@ -XX,X +XX,X @@ public class DedicatedServerProperties extends Settings<DedicatedServerPropertie
         this.queryPort = this.get("query.port", this.serverPort);
         this.enableRcon = this.get("enable-rcon", false);
         this.rconPort = this.get("rcon.port", 25575);
-        this.onlineMode = this.get("online-mode", true);
+        this.onlineMode = this.get("online-mode", false); // Paper - Set online-mode default to false
         this.allowFlight = this.get("allow-flight", false);
         this.motd = this.get("motd", "A Minecraft Server");
         this.forceGamemode = this.get("force-gamemode", false);

# by DEMORA

Оригинальный репозиторий PaperMC: https://github.com/PaperMC/Paper
# BY __DEMORA__

