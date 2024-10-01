---
title: ClearBanList
description: Membersihkan daftar ban
tags: ["administration"]
---

:::warning

Fungsi ini ditambahkan dalam omp v1.1.0.2612 dan tidak akan berfungsi pada versi sebelumnya!

:::

## Deskripsi

Membersihkan daftar ban

## Returns

**true** - Berhasil
**false** - Gagal menjalankan fungsi

## Contoh

```c
public OnPlayerCommandText(playerid, cmdtext[])
{
    if (!strcmp(cmdtext, "/clearbanlist", true))
    {
        if (!IsPlayerAdmin(playerid))
        {
            return 1;
        }

        ClearBanList();
        SendClientMessage(playerid, -1, "[SERVER]: List ban telah di bersihkan.");
        return 1;
    }
    return 0;
}
```

## Catatan

:::tip

Kamu juga bisa melihat list ban di file bans.json

:::


## Fungsi terkait
- [BlockIpAddress](BlockIpAddress): Blokir alamat IP agar tidak tersambung ke dalam server dalam jangka waktu tertentu
- [UnBlockIpAddress](UnBlockIpAddress): Membuka blokir IP yang sebelumnya di blokir
- [Ban](Ban): Melarang pemain bermain di server
- [BanEx](BanEx): Melarang pemain bermain di server dengan alasan khusus
- [Kick](Kick): Menendang pemain dari server
- [IsBanend](IsBanned): Memeriksa apakah alamat IP dilarang




