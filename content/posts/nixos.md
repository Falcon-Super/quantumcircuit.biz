+++
title = 'My NixOS Setup: ZFS, Impermanence, and Flakes'
date = 2024-09-24T15:31:15+03:00
draft = false
+++

When it comes to flexibility and declarative configurations, **NixOS** has been my go-to system for development. Over time, I’ve crafted a setup that balances stability, innovation, and minimal maintenance, all powered by a few key components: **ZFS on root**, **impermanence**, **flakes**, and **Home Manager**.

### ZFS on Root

One of the standout features of my NixOS configuration is **ZFS on root**. ZFS offers features like snapshots, compression, and data integrity, making it ideal for a system that demands reliability. Having ZFS as the root filesystem gives me peace of mind, especially when experimenting with new configurations or development tools.

### Impermanence: Inspired by "Erase Your Darlings"

My NixOS configuration embraces **impermanence**, inspired by the popular "Erase Your Darlings" blog post and others like it. The idea is simple: rather than storing state persistently, the system is designed to revert back to a clean slate, minimizing cruft and making it easier to maintain. Only the essential data that I explicitly want to keep survives between reboots, while everything else is wiped away.

By configuring directories like `/var` and `/etc` to be ephemeral, the system remains lean and tidy, forcing me to be more intentional with persistent changes. Combined with the flexibility of ZFS snapshots, this setup allows me to roll back quickly if things go awry.

### Flakes for Reproducibility

One of the core elements of my NixOS configuration is the **flake-based setup**. Flakes enable reproducibility and consistency, ensuring that my system can be built exactly the same way on any machine. Whether I’m setting up a new laptop or restoring an old configuration, I can rely on flakes to give me a precise, reproducible environment every time.

With the rise of flakes, managing packages, services, and configurations has become more modular and organized. I use flakes to manage everything from my system packages to my Home Manager setup, making it easier to tweak configurations and experiment without fear of breaking things.

### Home Manager for Personal Configurations

For user-specific configurations, I use **Home Manager**. It allows me to declaratively configure my home environment—everything from applications to dotfiles is managed in a single, version-controlled place. Home Manager integrates seamlessly with my flake setup, so I can tweak my personal environment while keeping my system config clean and isolated.

### GNOME vs. KDE Declarative Configuration

While I’ve had success configuring **GNOME** declaratively, **KDE** has been a bit of a mystery. I’ve struggled to get KDE working as declaratively as I’d like, even though GNOME works flawlessly in that regard. For now, I’ve opted to stick with GNOME for declarative setups, but I’m still on the lookout for a solution to get KDE configured just as smoothly.

---

That’s a quick overview of my NixOS journey so far. From ZFS on root to impermanence, flakes, and Home Manager, I’ve built a setup that’s robust, flexible, and easy to manage. There’s always more to learn and refine, but for now, I’m enjoying the power and simplicity that NixOS brings to the table.

---
