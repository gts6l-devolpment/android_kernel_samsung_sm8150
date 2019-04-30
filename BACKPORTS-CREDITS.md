# Galaxy Tab S6 (gts6l) — Android 17 / LineageOS 24.0 kernel backports: credits

Base: `lindofelix/android_kernel_samsung_gts6l` @ `lineage-22` (4.14.190).
Branch: `lineage-24.0-gts6l`. Total commits on top of base: **61** (60 backports/ adaptations + this credits document).

All entries below were applied with `git cherry-pick -x`, a Git 3-way merge (`git apply -3` + `git commit -C`), or `git commit` for the local adaptations. Original authorship is preserved in every case. The URL points to the public commit on GitHub or GitLab from which the change was sourced (including the GitLab mirror where applicable).

| Local SHA | Author | Subject | Original SHA | Source |
|---|---|---|---|---|
| `943bf3116e99` | `Christian Brauner` | `BACKPORT: fork: add clone3` | `929183edf055` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/929183edf05583b7099c4b9e4e058a38fbd2225d` |
| `e4da6cddd571` | `Christian Brauner` | `BACKPORT: arch: wire-up clone3() syscall` | `6b6446bf8c8a` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/6b6446bf8c8ae6b2f2507cb2d3c0f13a29c3c3a6` |
| `b987515ecaba` | `Christian Brauner` | `UPSTREAM: arch: handle arches who do not yet define clone3` | `50491e982250` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/50491e982250764b9e136320dfc189358c33b291` |
| `db907c0e2c54` | `Dmitry V. Levin` | `UPSTREAM: clone: fix CLONE_PIDFD support` | `64ab81d4ec03` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/64ab81d4ec03fd847d5d4831b415cdf077123cb9` |
| `60bf7ee00e21` | `Seth Forshee` | `UPSTREAM: sched: Add __ASSEMBLY__ guards around struct clone_args` | `03ee36377de9` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/03ee36377de9e31ce9b2f860f0f8242faa389790` |
| `ba96fe26b57b` | `Christian Brauner` | `UPSTREAM: sched: add kernel-doc for struct clone_args` | `1ad5ba777ad8` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/1ad5ba777ad8623b3383bde628ddbfd9ffbeee6e` |
| `5699c0af92a4` | `Christian Brauner` | `UPSTREAM: clone3: add CLONE_CLEAR_SIGHAND` | `545e7441a4d5` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/545e7441a4d57816746bb3a93b884df3622a3d41` |
| `0a833e19d37a` | `Christian Brauner` | `UPSTREAM: tests: test CLONE_CLEAR_SIGHAND` | `6fb6d5cc892e` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/6fb6d5cc892e7d1a5b7ea35dbf8e83d95c390c0b` |
| `e365381a3971` | `Adrian Reber` | `UPSTREAM: selftests: add tests for clone3()` | `e339db7e540b` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/e339db7e540b3b8152cf14f2ee8f61e67e2dab3f` |
| `20454a8484b0` | `Adrian Reber` | `UPSTREAM: capabilities: Introduce CAP_CHECKPOINT_RESTORE` | `0b2df1b8f72d` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/0b2df1b8f72de577810714d62c17b33e9180a724` |
| `58a1a2b4ff56` | `Adrian Reber` | `UPSTREAM: pid_namespace: use checkpoint_restore_ns_capable() for ns_last_pid` | `46ddbabd8bc7` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/46ddbabd8bc7e185d3fff8ae5d5e5445167ca865` |
| `1042dac8d38f` | `Adrian Reber` | `UPSTREAM: proc: allow access in init userns for map_files with CAP_CHECKPOINT_RESTORE` | `f60042219f92` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/f60042219f9235b72594273ff31c319672fded40` |
| `2e4ed8fecb8c` | `Michal Koutný` | `UPSTREAM: prctl_set_mm: refactor checks from validate_prctl_map` | `0ecb406d3e4d` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/0ecb406d3e4d1fb91a50e64ca754719c4c9779a9` |
| `29e650146267` | `Nicolas Viennot` | `UPSTREAM: prctl: Allow local CAP_CHECKPOINT_RESTORE to change /proc/self/exe` | `ae150ea33424` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/ae150ea33424672a1f6293ffad956ccc24d77155` |
| `3f69e210b693` | `Nicolas Viennot` | `UPSTREAM: prctl: exe link permission error changed from -EINVAL to -EPERM` | `27e46691dd1b` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/27e46691dd1bbcbc9c0fcd16a4bced7fed0face5` |
| `a02383f2eb9a` | `Adrian Reber` | `UPSTREAM: tty: allow TIOCSLCKTRMIOS with CAP_CHECKPOINT_RESTORE` | `6ae8d209ded5` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/6ae8d209ded5b86d820b92971b299931422d97cc` |
| `028bcf7b5a41` | `Aleksa Sarai` | `UPSTREAM: clone3: switch to copy_struct_from_user()` | `17a4db9ec43b` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/17a4db9ec43b7bc9421cb4edaa5ae51619544101` |
| `ee2506ba00d9` | `Christian Brauner` | `UPSTREAM: clone3: validate stack arguments` | `eb8eff544d75` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/eb8eff544d757eaec8f602380b0188c3a1f0eeeb` |
| `efe41b6cbad9` | `Amanieu d'Antras` | `UPSTREAM: arm64: Implement copy_thread_tls` | `d05a02bda12f` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/d05a02bda12f19b1ecf616828bc947fcdab3cec1` |
| `ad5d3a0f03f0` | `Sebastiano Barezzi` | `init: Add CONFIG_INITRAMFS_IGNORE_SKIP_FLAG` | `5110791d028a` | `https://github.com/LineageOS/android_kernel_oneplus_sm8150/commit/5110791d028aeae5c3e2a56043d95049cddd3b16` |
| `a9c13c8db919` | `Yumi Yukimura` | `fs: proc: Add PROC_CMDLINE_APPEND_ANDROID_FORCE_NORMAL_BOOT` | `74354d91fcf5` | `https://github.com/LineageOS/android_kernel_oneplus_sm8150/commit/74354d91fcf5d10689fe8fee65b4e13a61048249` |
| `8e402c64747b` | `ShevT` | `fs: proc: cmdline: Guard offset_addr and proc_command_line_tail` | `4b3045d8076e` | `https://github.com/LineageOS/android_kernel_oneplus_sm8150/commit/4b3045d8076e4304db185f74b6836d989bb75671` |
| `14bc938efc1d` | `Martin KaFai Lau` | `UPSTREAM: net: Change sock_getsockopt() to take the sk ptr instead of the sock ptr` | `193357db6a9b` | `(SHA 193357db6a9b568eba2e681a72e47666e81c8130; source to confirm)` |
| `718280897e81` | `Nick Desaulniers` | `BACKPORT: Makefile: infer --target from ARCH for CC=clang` | `dcf8a6327621` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/dcf8a6327621e8a009ca451c461e48218c28a1b8` |
| `68e8bd7bd4e5` | `Nathan Chancellor` | `UPSTREAM: Makefile: Remove '--gcc-toolchain' flag` | `7e94c1dfc885` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/7e94c1dfc885fc544b9aecbf24c9d79cf48dd62b` |
| `2f135c9892dd` | `Nick Desaulniers` | `Revert "ANDROID: Kbuild, LLVMLinux: allow overriding clang target triple"` | `628255e841b1` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/628255e841b108ae9268ee230bf5aaacb1259676` |
| `b66d8f874b83` | `Nick Desaulniers` | `BACKPORT: scripts/Makefile.clang: default to LLVM_IAS=1` | `ef2c4f5bbc63` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/ef2c4f5bbc636a7d432fb7fb2966f71f48b26d29` |
| `50283a3f9e9e` | `Sami Tolvanen` | `ANDROID: kallsyms: increase KSYM_NAME_LEN` | `25264dc9e8aa` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/25264dc9e8aa87d46559a25a0c8dfe2d2b6242fa` |
| `f8d0dd2ddfdc` | `Xiu Jianfeng` | `cgroup: Fix potential overflow issue when checking max_depth` | `7495cb605b36` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/7495cb605b36bb436f35f03c0db02061293ac0ed` |
| `10590327f042` | `Daniel Xu` | `UPSTREAM: kernfs: Add option to enable user xattrs` | `26cdb9faac26` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/26cdb9faac264738731a73946e1ba493fe2bfb30` |
| `2a49e3696b93` | `Daniel Xu` | `UPSTREAM: cgroupfs: Support user xattrs` | `c327eb4e3367` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/c327eb4e336713d9ce41a00f01af20105ff1a6fb` |
| `528bec0369ff` | `Roman Gushchin` | `UPSTREAM: cgroup: export list of delegatable control files using sysfs` | `5e20fbd42c38` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/5e20fbd42c38b2d2c8007dd1a4fd091a2d666682` |
| `b470d44e4989` | `Roman Gushchin` | `UPSTREAM: cgroup: export list of cgroups v2 features using sysfs` | `e2d18a7b42a2` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/e2d18a7b42a2b77b42ec615a31e4479e43f31d6f` |
| `bf7bdce8325f` | `Kirill Tkhai` | `BACKPORT: mm/memcontrol.c: export mem_cgroup_is_root()` | `f55ab8bb8687` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/f55ab8bb8687f83aa4144f671d97ea30559bf1f1` |
| `45e9fc3aed77` | `Wei Yang` | `UPSTREAM: cgroup: remove redundant kernfs_activate in cgroup_setup_root()` | `468ee8699ef1` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/468ee8699ef1b060383aaa6d1abc70f96be01743` |
| `403b79b2fa65` | `Tejun Heo` | `UPSTREAM: netprio: use css ID instead of cgroup ID` | `dbff509e40cd` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/dbff509e40cd75f04a212b92319167db0a29d93f` |
| `ded5eb286718` | `Tejun Heo` | `BACKPORT: cgroup: statically initialize init_css_set->dfl_cgrp` | `035af8fd1632` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/035af8fd163277629a45539ead8afe1f9ddf0bb5` |
| `c9789a08251f` | `Ma Shimiao` | `BACKPORT: cgroup: avoid copying strings longer than the buffers` | `76ff03abe048` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/76ff03abe0480be054b2bda90e4d44b61356930a` |
| `04af5062ae06` | `Arnd Bergmann` | `BACKPORT: cgroup: use strlcpy() instead of strscpy() to avoid spurious warning` | `f02be96a66d7` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/f02be96a66d72e05a82b495ded374d445f9033d6` |
| `99e8e94fdb39` | `Tejun Heo` | `BACKPORT: string: drop __must_check from strscpy() and restore strscpy() usages in cgroup` | `d9bb2f98f813` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/d9bb2f98f813b60b98e59b1770fc7efdcfa5db7c` |
| `4fbf0b5fb143` | `Roman Gushchin` | `BACKPORT: cgroup: make cgroup.threads delegatable` | `ebe4028eb8e3` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/ebe4028eb8e3960559eee1f6a57f3a8c22c0c2db` |
| `57b01d5418bb` | `Matt Roper` | `BACKPORT: cgroup: Update documentation reference` | `fd2c63aea45c` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/fd2c63aea45c7af7e02e1af4176f888c4fc60125` |
| `331c400ce982` | `Tejun Heo` | `BACKPORT: cgroup: Explicitly remove core interface files` | `7b18c4206452` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/7b18c42064529d0b96e9676238d412b104090002` |
| `ba58a65dfb1f` | `Tejun Heo` | `UPSTREAM: cgroup: add cgroup_parse_float()` | `d201d78b8ecc` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/d201d78b8eccebbb63a111b1897424a3910ec64c` |
| `73a15a6321fb` | `Yangtao Li` | `BACKPORT: cgroup: remove unnecessary unlikely()` | `16aade1935d3` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/16aade1935d318cb5f3b63eef02bce6bfc6c8c69` |
| `9d783c0566b7` | `Tejun Heo` | `BACKPORT: cgroup: Add named hierarchy disabling to cgroup_no_v1 boot param` | `242869ba7e71` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/242869ba7e71a3598307695bd5bafe72b3db4d0a` |
| `7c4384509a2a` | `Al Viro` | `BACKPORT: cgroup: saner refcounting for cgroup_root` | `a98f9986011e` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/a98f9986011e09be4d78a85a69d2cdf01988736e` |
| `deac41eb04a0` | `Shakeel Butt` | `BACKPORT: cgroup: remove extra cgroup_migrate_finish() call` | `fda7b4bc3127` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/fda7b4bc3127dfed24348b01bb1b39f656a3990d` |
| `a766b6feaf2d` | `Chen Ridong` | `UPSTREAM: cgroup/bpf: only cgroup v2 can be attached by bpf programs` | `0674265f7cd0` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/0674265f7cd0af2c46dd4e440869bb2e95c22017` |
| `58dba0db9b39` | `Jian Cai` | `arm64: vdso: remove commas between macro name and arguments` | `d2a5f4a03570` | `https://github.com/keremkt38/ErciyesKernel-a50/commit/d2a5f4a035701c32983f63f8c531fa987c5dec23` |
| `70497576b74d` | Cameron | ANDROID: Makefile: add LLVM=1 support for GCC-free builds | — | local adaptation |
| `be1b80c92e78` | Cameron | arm64: gts6l: enable Android 17 / LineageOS 24.0 kernel options | — | local adaptation |
| `425e54bddd97` | `Aleksa Sarai` | `BACKPORT: lib: introduce copy_struct_from_user() helper` | `34d39a21006b` | `https://github.com/iput-object/kernel_xiaomi_sm6250/commit/34d39a21006bf7cb0bb61b85e6bb28d1d578dc2c` |
| `fdf51c076ebd` | `Adrian Reber` | `UPSTREAM: fork: extend clone3() to support setting a PID` | `049a15b97f3d` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/049a15b97f3d5294ae193f53abec9d30442c6d53` |
| `6e37c51eee48` | Cameron | cgroup: adapt bpf v2-only backport to stock 4.14 BPF API | — | local adaptation |
| `9faf47577d49` | `Junxi Qian` | `UPSTREAM: nfc: llcp: add missing return after LLCP_CLOSED checks` | `69dd158b1370` | `https://gitlab.com/xusu616/android_kernel_oneplus_sm8150/-/commit/69dd158b1370a155b89318d286da6a6152c7d142` |
| `989332e6c17d` | `UDPSendToFailed` | `cgroup: backport cgroup v2 freezer` | `f65fb9cfd2fd` | `https://github.com/UDPSendToFailed/android_kernel_samsung_gta2xlwifi/commit/f65fb9cfd2fd79e7735ae3301e437280aeb0cb12` |
| `79cb0352a8ff` | `Roman Gushchin` | `BACKPORT: cgroup: freezer: fix frozen state inheritance` | `c82d883e6f02` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/c82d883e6f02ddae76801bf2788530f9e41519e6` |
| `4fcb3a3ef9a7` | `Oleg Nesterov` | `BACKPORT: cgroup: freezer: call cgroup_enter_frozen() with preemption disabled in ptrace_stop()` | `957c39896c14` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/957c39896c14030d2a466c4cab58302ab5f620b3` |
| `7958544930e1` | `Roman Gushchin` | `BACKPORT: signal: unconditionally leave the frozen state in ptrace_stop()` | `f4655d5501e1` | `https://github.com/LineageOS/android_kernel_qcom_sm8150/commit/f4655d5501e1cf9fe754de397e84c5dd304dc974` |

## Skipped / adapted commits

- `d813f35527c` — already present in base (no commit needed).
- `7a4a0bb6c4e`, `c4d3b3ec180`, `d0e8ec39ab8` — vendor defconfig-only changes; not applicable.
- `8b35db58e3e`, `f8fa654ae17`, `d6b4808619e` — eBPF/sockptr series dropped: base BPF lacks `sockptr_t`, `rcu_read_lock_trace_held()`, `is_spilled_reg()`. The self-contained `copy_struct_from_user()` helper and `1984bf177b6` (`sock_getsockopt`) were kept.
- `0eaf911a220` (memcg `memory.events` subtrees), `b3f11c33f7f` (`cgroup_ino` WARN_ON) — conflict with the Samsung 4.14 cgroup/memcg layout; not applied.
- `7a05073b02d`, `28586903263` — written for Google's v2-freezer variant in `kernel/cgroup/freezer.c`; the Samsung jobctl-trap freezer backport used here implements the same feature with a different internal API.
- `967629779d4` — cherry-pick resulted in an empty patch (equivalent cleanup already present).
- EROFS: already enabled (`CONFIG_EROFS_FS=y`, xattrs/ACL/security/ZIP); no discrete EROFS commits exist in the tracked upstream branches.

## Verification

- `make ARCH=arm64 LLVM=1 LLVM_IAS=1 gts6l_eur_open_defconfig` — OK.
- clang object builds: `kernel/fork.o`, `kernel/pid.o`, `kernel/signal.o`, `kernel/cgroup/cgroup.o`, `kernel/cgroup/freezer.o`, `kernel/bpf/cgroup.o`, `lib/usercopy.o`, `init/initramfs.o`, `fs/proc/cmdline.o` — OK.
- clone3 syscall wired for arm64 and arm32 (`__NR_clone3 435`), `CAP_CHECKPOINT_RESTORE` defined.
- `CONFIG_INITRAMFS_IGNORE_SKIP_FLAG`, `CONFIG_PROC_CMDLINE_APPEND_ANDROID_FORCE_NORMAL_BOOT`, `CONFIG_BPF_JIT(_ALWAYS_ON)` enabled in `gts6l_eur_open_defconfig`.
