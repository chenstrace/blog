---
title: How to fix and recover a corrupt history file in zsh
tags:
  - zsh 
categories:
  - 工程实践 
date: 2016-01-26 10:22:43
---

	cd ~
	mv .zsh_history .zsh_history_bad
	strings .zsh_history_bad > .zsh_history
	fc -R .zsh_history
