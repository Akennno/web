---
title: ClearBanList
description: Menghapus semua list ban
tags: ["administration"]
---
:::warning 

ungsi ini ditambahkan dalam omp v1.1.0.2612 dan tidak akan berfungsi pada versi sebelumnya!

:::

## Deskripsi

Menghapus semua list ban

## Returns 

**true** - Berhasil
**false** - Gagal

## Contoh
```c
public OnPlayerCommandText(playerid, cmdtext[])
{
  if(!strcmp(cmdtext, "/clearbanlist", true))
  {
    if(!IsPlayerAdmin(playerid))
    {
      return 1;
    }
    ClearBanList();
    SendClientMessage(playerid, -1, "[SERVER]: Ban list cleared.");
    return 1;
  }
  return 0;
}
```

## Catatan


:::tip

Kamu juga dapat melihat daftar larangan di berkas bans.json

:::

## Fungsi Terkait

- [BlockIpAddress](BlockIpAddress): Memblokir ip address agar tidak bisa tersambung ke server selama jangka waktu yang ditentukan
- [UnBlockIpAddres](UnBlockIpAddress): Membuka blokir ip address yang sebelumnya terkena blokir
- [Ban](Ban): Melarang pemain bermain di server
- [BanEx](BanEx): Melarang pemain dengan alasan khusus
- [Kick](Kick) Menendang player dari server  
- [IsBanned](IsBanned) Memeriksa apakah alamat Ip Address dilarang tersambung ke server
