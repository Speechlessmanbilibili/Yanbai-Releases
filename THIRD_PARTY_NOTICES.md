# Third-Party Notices

Yanbai (砚白) incorporates the third-party components listed below. They are distributed in binary form as part of the Software and remain governed by their own license terms; nothing in the Yanbai End User License Agreement modifies or replaces those terms.

本文件列出随砚白以二进制形式分发的第三方组件，各组件仍适用其自身的许可条款，《砚白最终用户使用许可协议》不改变也不替代这些条款。

## How this list is built / 清单的生成方式

- Rust crates: the normal dependency graph of the Yanbai application for the four shipped targets (windows-msvc x64/arm64, linux-gnu x64/arm64), resolved from Cargo.lock. Build-time-only and other-platform dependencies are excluded.
- Frontend packages: the installed production dependency tree corresponding to frontend/pnpm-lock.yaml, excluding type-only packages (@types/*).
- 中文：Rust 侧按 Cargo.lock 解析四个交付目标的应用普通依赖图；前端使用与锁文件一致的生产依赖树，排除纯类型包。不同版本或来源分别列出。
- Original license expressions are preserved. The Selected column uses explicit, reviewed entries in tools/notices-policy.json; unknown composite expressions or missing license metadata stop generation for manual review.
- 中文：保留原始许可表达式，“Selected”列按受版本管理的显式配置选择；未登记的复合表达式或缺少许可的组件会使生成中止，等待人工核对。
- Components under MPL-2.0 and LGPL are used unmodified; their source is available from the component’s published distribution (crates.io or npm).

## Rust crates (378)

| Component | Version | Source | Licenses | Selected |
| --- | --- | --- | --- | --- |
| adler2 | 2.0.1 | registry+https://github.com/rust-lang/crates.io-index | 0BSD OR MIT OR Apache-2.0 | MIT |
| aead | 0.5.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| aes | 0.8.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| aes-gcm | 0.10.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| aho-corasick | 1.1.5 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| alloc-no-stdlib | 2.0.4 | registry+https://github.com/rust-lang/crates.io-index | BSD-3-Clause | BSD-3-Clause |
| alloc-stdlib | 0.2.4 | registry+https://github.com/rust-lang/crates.io-index | BSD-3-Clause | BSD-3-Clause |
| anyhow | 1.0.104 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| async-broadcast | 0.7.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| async-channel | 2.5.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| async-executor | 1.14.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| async-io | 2.6.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| async-lock | 3.4.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| async-process | 2.5.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| async-recursion | 1.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| async-signal | 0.2.14 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| async-task | 4.7.1 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| async-trait | 0.1.92 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| atk | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| atk-sys | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| atomic-waker | 1.1.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| base64 | 0.22.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| base64 | 0.23.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| bit-set | 0.8.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| bit-vec | 0.8.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| bitflags | 1.3.2 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| bitflags | 2.13.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| block-buffer | 0.10.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| blocking | 1.7.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| brotli | 8.0.4 | registry+https://github.com/rust-lang/crates.io-index | BSD-3-Clause AND MIT | BSD-3-Clause AND MIT |
| brotli-decompressor | 5.0.3 | registry+https://github.com/rust-lang/crates.io-index | BSD-3-Clause/MIT | MIT |
| bs58 | 0.5.1 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| bumpalo | 3.20.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| byteorder | 1.5.0 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| bytes | 1.12.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| cairo-rs | 0.18.5 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| cairo-sys-rs | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| camino | 1.2.5 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| cargo-platform | 0.1.9 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| cargo_metadata | 0.19.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| cfb | 0.7.3 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| cfg-if | 1.0.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| chardetng | 0.1.17 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| chrono | 0.4.45 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| cipher | 0.4.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| concurrent-queue | 2.5.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| cookie | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| core_detect | 1.0.0 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| cpufeatures | 0.2.17 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| crc32fast | 1.5.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| crossbeam-channel | 0.5.17 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| crossbeam-utils | 0.8.23 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| crypto-common | 0.1.7 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| cssparser | 0.36.0 | registry+https://github.com/rust-lang/crates.io-index | MPL-2.0 | MPL-2.0 |
| cssparser-macros | 0.6.1 | registry+https://github.com/rust-lang/crates.io-index | MPL-2.0 | MPL-2.0 |
| ctor | 0.8.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| ctor-proc-macro | 0.0.7 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| ctr | 0.9.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| darling | 0.23.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| darling_core | 0.23.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| darling_macro | 0.23.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| dbus | 0.9.12 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0/MIT | MIT |
| defmt | 1.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| defmt-macros | 1.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| defmt-parser | 1.0.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| deranged | 0.5.8 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| derive_more | 2.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| derive_more-impl | 2.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| digest | 0.10.7 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| dirs | 6.0.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| dirs-sys | 0.5.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| displaydoc | 0.2.7 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| dlopen2 | 0.8.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| dlopen2_derive | 0.4.3 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| dom_query | 0.27.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| dpi | 0.1.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 AND MIT | Apache-2.0 AND MIT |
| dtoa | 1.0.11 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| dtoa-short | 0.3.5 | registry+https://github.com/rust-lang/crates.io-index | MPL-2.0 | MPL-2.0 |
| dtor | 0.3.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| dtor-proc-macro | 0.0.6 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| dunce | 1.0.5 | registry+https://github.com/rust-lang/crates.io-index | CC0-1.0 OR MIT-0 OR Apache-2.0 | Apache-2.0 |
| dyn-clone | 1.0.20 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| encoding_rs | 0.8.40 | registry+https://github.com/rust-lang/crates.io-index | (Apache-2.0 OR MIT) AND BSD-3-Clause | MIT AND BSD-3-Clause |
| endi | 1.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| enumflags2 | 0.7.12 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| enumflags2_derive | 0.7.12 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| equivalent | 1.0.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| erased-serde | 0.4.10 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| errno | 0.3.14 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| event-listener | 5.4.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| event-listener-strategy | 0.5.4 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| fastrand | 2.5.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| fdeflate | 0.3.7 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| fern | 0.7.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| field-offset | 0.3.6 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| flate2 | 1.1.10 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| fnv | 1.0.7 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 / MIT | MIT |
| foldhash | 0.2.0 | registry+https://github.com/rust-lang/crates.io-index | Zlib | Zlib |
| form_urlencoded | 1.2.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-channel | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-core | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-executor | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-io | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-lite | 2.6.1 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| futures-macro | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-sink | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-task | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| futures-util | 0.3.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| gdk | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gdk-pixbuf | 0.18.5 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gdk-pixbuf-sys | 0.18.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gdk-sys | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gdkwayland-sys | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gdkx11 | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gdkx11-sys | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| generic-array | 0.14.7 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| getrandom | 0.2.17 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| getrandom | 0.3.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| getrandom | 0.4.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| ghash | 0.5.1 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| gio | 0.18.4 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gio-sys | 0.18.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| glib | 0.18.5 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| glib-macros | 0.18.5 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| glib-sys | 0.18.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| glob | 0.3.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| gobject-sys | 0.18.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gtk | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gtk-sys | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| gtk3-macros | 0.18.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| hashbrown | 0.12.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| hashbrown | 0.17.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| heck | 0.4.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| heck | 0.5.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| hex | 0.4.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| html5ever | 0.38.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| http | 1.5.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| iana-time-zone | 0.1.65 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| ico | 0.5.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| icu_collections | 2.3.0 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| icu_locale_core | 2.3.0 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| icu_normalizer | 2.3.0 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| icu_normalizer_data | 2.3.0 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| icu_properties | 2.3.0 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| icu_properties_data | 2.3.0 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| icu_provider | 2.3.1 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| ident_case | 1.0.1 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| idna | 1.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| idna_adapter | 1.2.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| indexmap | 1.9.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| indexmap | 2.14.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| infer | 0.19.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| inout | 0.1.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| itoa | 1.0.18 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| javascriptcore-rs | 1.1.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| javascriptcore-rs-sys | 1.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| jiff | 0.2.35 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| jiff-core | 0.1.0 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| jiff-tzdb | 0.1.8 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| jiff-tzdb-platform | 0.1.3 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| json-patch | 3.0.1 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| jsonptr | 0.6.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| keyboard-types | 0.7.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| libappindicator | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| libappindicator-sys | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| libc | 0.2.189 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| libdbus-sys | 0.2.7 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0/MIT | MIT |
| libloading | 0.7.4 | registry+https://github.com/rust-lang/crates.io-index | ISC | ISC |
| linux-raw-sys | 0.12.1 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 WITH LLVM-exception OR Apache-2.0 OR MIT | MIT |
| litemap | 0.8.3 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| lock_api | 0.4.14 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| log | 0.4.34 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| markup5ever | 0.38.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| memchr | 2.8.3 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| memoffset | 0.9.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| mime | 0.3.17 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| miniz_oxide | 0.8.9 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Zlib OR Apache-2.0 | MIT |
| miniz_oxide | 0.9.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Zlib OR Apache-2.0 | MIT |
| mio | 1.2.3 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| muda | 0.19.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| multiversion | 0.8.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| multiversion-macros | 0.8.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| multiversion_no_op | 1.0.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| new_debug_unreachable | 1.0.6 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| num-conv | 0.2.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| num-traits | 0.2.19 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| num_threads | 0.1.7 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| once_cell | 1.21.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| opaque-debug | 0.3.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| option-ext | 0.2.0 | registry+https://github.com/rust-lang/crates.io-index | MPL-2.0 | MPL-2.0 |
| ordered-stream | 0.2.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| pango | 0.18.3 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| pango-sys | 0.18.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| parking | 2.2.1 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| parking_lot | 0.12.5 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| parking_lot_core | 0.9.12 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| percent-encoding | 2.3.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| phf | 0.13.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| phf_generator | 0.13.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| phf_macros | 0.13.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| phf_shared | 0.13.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| pin-project-lite | 0.2.17 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| piper | 0.2.5 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| plist | 1.10.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| png | 0.17.16 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| png | 0.18.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| polling | 3.11.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| polyval | 0.6.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| potential_utf | 0.1.6 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| powerfmt | 0.2.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| precomputed-hash | 0.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| proc-macro-crate | 1.3.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| proc-macro-crate | 2.0.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| proc-macro-crate | 3.5.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| proc-macro-error | 1.0.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| proc-macro-error-attr | 1.0.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| proc-macro2 | 1.0.107 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| quick-xml | 0.37.5 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| quick-xml | 0.42.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| quote | 1.0.47 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| rand_core | 0.6.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| raw-window-handle | 0.6.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 OR Zlib | MIT |
| ref-cast | 1.0.27 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| ref-cast-impl | 1.0.27 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| regex | 1.13.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| regex-automata | 0.4.18 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| regex-syntax | 0.8.11 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| rfd | 0.16.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| roxmltree | 0.21.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| rustc-hash | 2.1.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| rustix | 1.1.4 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 WITH LLVM-exception OR Apache-2.0 OR MIT | MIT |
| same-file | 1.0.6 | registry+https://github.com/rust-lang/crates.io-index | Unlicense/MIT | MIT |
| schemars | 0.8.22 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| schemars | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| schemars | 1.2.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| schemars_derive | 0.8.22 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| scopeguard | 1.2.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| selectors | 0.36.1 | registry+https://github.com/rust-lang/crates.io-index | MPL-2.0 | MPL-2.0 |
| semver | 1.0.28 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde | 1.0.229 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde-untagged | 0.1.9 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_core | 1.0.229 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_derive | 1.0.229 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_derive_internals | 0.29.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_json | 1.0.151 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_repr | 0.1.21 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_spanned | 0.6.9 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_spanned | 1.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_with | 3.22.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serde_with_macros | 3.22.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serialize-to-javascript | 0.1.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| serialize-to-javascript-impl | 0.1.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| servo_arc | 0.4.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| sha2 | 0.10.9 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| signal-hook-registry | 1.4.8 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| simd-adler32 | 0.3.10 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| simdutf8 | 0.1.5 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| siphasher | 1.0.3 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| slab | 0.4.12 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| smallvec | 1.16.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| socket2 | 0.6.5 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| softbuffer | 0.4.8 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| soup3 | 0.5.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| soup3-sys | 0.5.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| stable_deref_trait | 1.2.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| string_cache | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| strsim | 0.11.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| subtle | 2.6.1 | registry+https://github.com/rust-lang/crates.io-index | BSD-3-Clause | BSD-3-Clause |
| syn | 1.0.109 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| syn | 2.0.119 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| syn | 3.0.5 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| synstructure | 0.13.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| tao | 0.35.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 | Apache-2.0 |
| target-features | 0.1.6 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| tauri | 2.11.5 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-codegen | 2.6.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-macros | 2.6.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-plugin-dialog | 2.7.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-plugin-fs | 2.5.2 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-plugin-log | 2.9.1 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-plugin-single-instance | 2.4.4 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-runtime | 2.11.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-runtime-wry | 2.11.4 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tauri-utils | 2.9.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| tempfile | 3.27.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| tendril | 0.5.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| thiserror | 1.0.69 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| thiserror | 2.0.20 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| thiserror-impl | 1.0.69 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| thiserror-impl | 2.0.20 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| time | 0.3.55 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| time-core | 0.1.9 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| time-macros | 0.2.32 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| tinystr | 0.8.4 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| tinyvec | 1.13.2 | registry+https://github.com/rust-lang/crates.io-index | Zlib OR Apache-2.0 OR MIT | MIT |
| tinyvec_macros | 0.1.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 OR Zlib | MIT |
| tokio | 1.53.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| toml | 1.1.5+spec-1.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| toml_datetime | 0.6.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| toml_datetime | 1.1.1+spec-1.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| toml_edit | 0.19.15 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| toml_edit | 0.20.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| toml_edit | 0.25.13+spec-1.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| toml_parser | 1.1.3+spec-1.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| toml_writer | 1.1.2+spec-1.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| tracing | 0.1.44 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| tracing-attributes | 0.1.31 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| tracing-core | 0.1.36 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| tray-icon | 0.24.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| typeid | 1.0.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| typenum | 1.20.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| unic-char-property | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| unic-char-range | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| unic-common | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| unic-ucd-ident | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| unic-ucd-version | 0.9.0 | registry+https://github.com/rust-lang/crates.io-index | MIT/Apache-2.0 | MIT |
| unicode-ident | 1.0.24 | registry+https://github.com/rust-lang/crates.io-index | (MIT OR Apache-2.0) AND Unicode-3.0 | MIT AND Unicode-3.0 |
| unicode-segmentation | 1.13.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| universal-hash | 0.5.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| url | 2.5.8 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| urlpattern | 0.3.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| utf8_iter | 1.0.4 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| uuid | 1.26.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| walkdir | 2.5.0 | registry+https://github.com/rust-lang/crates.io-index | Unlicense/MIT | MIT |
| web_atoms | 0.2.6 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| webkit2gtk | 2.0.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| webkit2gtk-sys | 2.0.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| webview2-com | 0.38.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| webview2-com-macros | 0.8.1 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| webview2-com-sys | 0.38.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| winapi-util | 0.1.11 | registry+https://github.com/rust-lang/crates.io-index | Unlicense OR MIT | MIT |
| window-vibrancy | 0.6.0 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| windows | 0.61.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-collections | 0.2.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-core | 0.61.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-future | 0.2.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-implement | 0.60.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-interface | 0.59.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-link | 0.1.3 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-link | 0.2.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-numerics | 0.2.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-result | 0.3.4 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-strings | 0.4.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-sys | 0.59.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-sys | 0.60.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-sys | 0.61.2 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-targets | 0.52.6 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-targets | 0.53.5 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-threading | 0.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows-version | 0.1.7 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows_aarch64_msvc | 0.52.6 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows_aarch64_msvc | 0.53.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows_x86_64_msvc | 0.52.6 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| windows_x86_64_msvc | 0.53.1 | registry+https://github.com/rust-lang/crates.io-index | MIT OR Apache-2.0 | MIT |
| winnow | 0.5.40 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| winnow | 1.0.4 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| writeable | 0.6.4 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| wry | 0.55.1 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 OR MIT | MIT |
| x11 | 2.21.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| x11-dl | 2.21.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| yoke | 0.8.3 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| yoke-derive | 0.8.2 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| zbus | 5.19.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zbus_macros | 5.19.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zbus_names | 4.3.4 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zcheapstr | 1.1.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zerofrom | 0.1.8 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| zerofrom-derive | 0.1.7 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| zerotrie | 0.2.5 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| zerovec | 0.11.8 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| zerovec-derive | 0.11.6 | registry+https://github.com/rust-lang/crates.io-index | Unicode-3.0 | Unicode-3.0 |
| zip | 2.4.2 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zlib-rs | 0.6.7 | registry+https://github.com/rust-lang/crates.io-index | Zlib | Zlib |
| zmij | 1.0.23 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zopfli | 0.8.3 | registry+https://github.com/rust-lang/crates.io-index | Apache-2.0 | Apache-2.0 |
| zvariant | 5.15.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zvariant_derive | 5.15.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |
| zvariant_utils | 4.2.0 | registry+https://github.com/rust-lang/crates.io-index | MIT | MIT |

## Frontend packages (91)

| Component | Version | Source | Licenses | Selected |
| --- | --- | --- | --- | --- |
| @antfu/install-pkg | 2.0.1 | https://registry.npmjs.org/@antfu/install-pkg/-/install-pkg-2.0.1.tgz | MIT | MIT |
| @braintree/sanitize-url | 7.1.2 | https://registry.npmjs.org/@braintree/sanitize-url/-/sanitize-url-7.1.2.tgz | MIT | MIT |
| @chevrotain/types | 11.1.2 | https://registry.npmjs.org/@chevrotain/types/-/types-11.1.2.tgz | Apache-2.0 | Apache-2.0 |
| @iconify/types | 2.0.0 | https://registry.npmjs.org/@iconify/types/-/types-2.0.0.tgz | MIT | MIT |
| @iconify/utils | 3.1.6 | https://registry.npmjs.org/@iconify/utils/-/utils-3.1.6.tgz | MIT | MIT |
| @mermaid-js/parser | 1.2.1 | https://registry.npmjs.org/@mermaid-js/parser/-/parser-1.2.1.tgz | MIT | MIT |
| @tauri-apps/api | 2.11.1 | https://registry.npmjs.org/@tauri-apps/api/-/api-2.11.1.tgz | Apache-2.0 OR MIT | MIT |
| @tauri-apps/plugin-dialog | 2.7.3 | https://registry.npmjs.org/@tauri-apps/plugin-dialog/-/plugin-dialog-2.7.3.tgz | MIT OR Apache-2.0 | MIT |
| @tauri-apps/plugin-fs | 2.5.2 | https://registry.npmjs.org/@tauri-apps/plugin-fs/-/plugin-fs-2.5.2.tgz | MIT OR Apache-2.0 | MIT |
| @upsetjs/venn.js | 2.0.0 | https://registry.npmjs.org/@upsetjs/venn.js/-/venn.js-2.0.0.tgz | MIT | MIT |
| clsx | 2.1.1 | https://registry.npmjs.org/clsx/-/clsx-2.1.1.tgz | MIT | MIT |
| commander | 15.0.0 | https://registry.npmjs.org/commander/-/commander-15.0.0.tgz | MIT | MIT |
| commander | 7.2.0 | https://registry.npmjs.org/commander/-/commander-7.2.0.tgz | MIT | MIT |
| commander | 8.3.0 | https://registry.npmjs.org/commander/-/commander-8.3.0.tgz | MIT | MIT |
| cose-base | 1.0.3 | https://registry.npmjs.org/cose-base/-/cose-base-1.0.3.tgz | MIT | MIT |
| cose-base | 2.2.0 | https://registry.npmjs.org/cose-base/-/cose-base-2.2.0.tgz | MIT | MIT |
| cytoscape | 3.34.2 | https://registry.npmjs.org/cytoscape/-/cytoscape-3.34.2.tgz | MIT | MIT |
| cytoscape-cose-bilkent | 4.1.0 | https://registry.npmjs.org/cytoscape-cose-bilkent/-/cytoscape-cose-bilkent-4.1.0.tgz | MIT | MIT |
| cytoscape-fcose | 2.2.0 | https://registry.npmjs.org/cytoscape-fcose/-/cytoscape-fcose-2.2.0.tgz | MIT | MIT |
| d3 | 7.9.0 | https://registry.npmjs.org/d3/-/d3-7.9.0.tgz | ISC | ISC |
| d3-array | 2.12.1 | https://registry.npmjs.org/d3-array/-/d3-array-2.12.1.tgz | BSD-3-Clause | BSD-3-Clause |
| d3-array | 3.2.4 | https://registry.npmjs.org/d3-array/-/d3-array-3.2.4.tgz | ISC | ISC |
| d3-axis | 3.0.0 | https://registry.npmjs.org/d3-axis/-/d3-axis-3.0.0.tgz | ISC | ISC |
| d3-brush | 3.0.0 | https://registry.npmjs.org/d3-brush/-/d3-brush-3.0.0.tgz | ISC | ISC |
| d3-chord | 3.0.1 | https://registry.npmjs.org/d3-chord/-/d3-chord-3.0.1.tgz | ISC | ISC |
| d3-color | 3.1.0 | https://registry.npmjs.org/d3-color/-/d3-color-3.1.0.tgz | ISC | ISC |
| d3-contour | 4.0.2 | https://registry.npmjs.org/d3-contour/-/d3-contour-4.0.2.tgz | ISC | ISC |
| d3-delaunay | 6.0.4 | https://registry.npmjs.org/d3-delaunay/-/d3-delaunay-6.0.4.tgz | ISC | ISC |
| d3-dispatch | 3.0.1 | https://registry.npmjs.org/d3-dispatch/-/d3-dispatch-3.0.1.tgz | ISC | ISC |
| d3-drag | 3.0.0 | https://registry.npmjs.org/d3-drag/-/d3-drag-3.0.0.tgz | ISC | ISC |
| d3-dsv | 3.0.1 | https://registry.npmjs.org/d3-dsv/-/d3-dsv-3.0.1.tgz | ISC | ISC |
| d3-ease | 3.0.1 | https://registry.npmjs.org/d3-ease/-/d3-ease-3.0.1.tgz | BSD-3-Clause | BSD-3-Clause |
| d3-fetch | 3.0.1 | https://registry.npmjs.org/d3-fetch/-/d3-fetch-3.0.1.tgz | ISC | ISC |
| d3-force | 3.0.0 | https://registry.npmjs.org/d3-force/-/d3-force-3.0.0.tgz | ISC | ISC |
| d3-format | 3.1.2 | https://registry.npmjs.org/d3-format/-/d3-format-3.1.2.tgz | ISC | ISC |
| d3-geo | 3.1.1 | https://registry.npmjs.org/d3-geo/-/d3-geo-3.1.1.tgz | ISC | ISC |
| d3-hierarchy | 3.1.2 | https://registry.npmjs.org/d3-hierarchy/-/d3-hierarchy-3.1.2.tgz | ISC | ISC |
| d3-interpolate | 3.0.1 | https://registry.npmjs.org/d3-interpolate/-/d3-interpolate-3.0.1.tgz | ISC | ISC |
| d3-path | 1.0.9 | https://registry.npmjs.org/d3-path/-/d3-path-1.0.9.tgz | BSD-3-Clause | BSD-3-Clause |
| d3-path | 3.1.0 | https://registry.npmjs.org/d3-path/-/d3-path-3.1.0.tgz | ISC | ISC |
| d3-polygon | 3.0.1 | https://registry.npmjs.org/d3-polygon/-/d3-polygon-3.0.1.tgz | ISC | ISC |
| d3-quadtree | 3.0.1 | https://registry.npmjs.org/d3-quadtree/-/d3-quadtree-3.0.1.tgz | ISC | ISC |
| d3-random | 3.0.1 | https://registry.npmjs.org/d3-random/-/d3-random-3.0.1.tgz | ISC | ISC |
| d3-sankey | 0.12.3 | https://registry.npmjs.org/d3-sankey/-/d3-sankey-0.12.3.tgz | BSD-3-Clause | BSD-3-Clause |
| d3-scale | 4.0.2 | https://registry.npmjs.org/d3-scale/-/d3-scale-4.0.2.tgz | ISC | ISC |
| d3-scale-chromatic | 3.1.0 | https://registry.npmjs.org/d3-scale-chromatic/-/d3-scale-chromatic-3.1.0.tgz | ISC | ISC |
| d3-selection | 3.0.0 | https://registry.npmjs.org/d3-selection/-/d3-selection-3.0.0.tgz | ISC | ISC |
| d3-shape | 1.3.7 | https://registry.npmjs.org/d3-shape/-/d3-shape-1.3.7.tgz | BSD-3-Clause | BSD-3-Clause |
| d3-shape | 3.2.0 | https://registry.npmjs.org/d3-shape/-/d3-shape-3.2.0.tgz | ISC | ISC |
| d3-time | 3.1.0 | https://registry.npmjs.org/d3-time/-/d3-time-3.1.0.tgz | ISC | ISC |
| d3-time-format | 4.1.0 | https://registry.npmjs.org/d3-time-format/-/d3-time-format-4.1.0.tgz | ISC | ISC |
| d3-timer | 3.0.1 | https://registry.npmjs.org/d3-timer/-/d3-timer-3.0.1.tgz | ISC | ISC |
| d3-transition | 3.0.1 | https://registry.npmjs.org/d3-transition/-/d3-transition-3.0.1.tgz | ISC | ISC |
| d3-zoom | 3.0.0 | https://registry.npmjs.org/d3-zoom/-/d3-zoom-3.0.0.tgz | ISC | ISC |
| dagre-d3-es | 7.0.14 | https://registry.npmjs.org/dagre-d3-es/-/dagre-d3-es-7.0.14.tgz | MIT | MIT |
| dayjs | 1.11.23 | https://registry.npmjs.org/dayjs/-/dayjs-1.11.23.tgz | MIT | MIT |
| delaunator | 5.1.0 | https://registry.npmjs.org/delaunator/-/delaunator-5.1.0.tgz | ISC | ISC |
| dompurify | 3.4.15 | https://registry.npmjs.org/dompurify/-/dompurify-3.4.15.tgz | (MPL-2.0 OR Apache-2.0) | Apache-2.0 |
| es-toolkit | 1.52.0 | https://registry.npmjs.org/es-toolkit/-/es-toolkit-1.52.0.tgz | MIT | MIT |
| fastdom | 1.0.12 | https://registry.npmjs.org/fastdom/-/fastdom-1.0.12.tgz | MIT | MIT |
| hachure-fill | 0.5.2 | https://registry.npmjs.org/hachure-fill/-/hachure-fill-0.5.2.tgz | MIT | MIT |
| iconv-lite | 0.6.3 | https://registry.npmjs.org/iconv-lite/-/iconv-lite-0.6.3.tgz | MIT | MIT |
| import-meta-resolve | 4.2.0 | https://registry.npmjs.org/import-meta-resolve/-/import-meta-resolve-4.2.0.tgz | MIT | MIT |
| internmap | 1.0.1 | https://registry.npmjs.org/internmap/-/internmap-1.0.1.tgz | ISC | ISC |
| internmap | 2.0.3 | https://registry.npmjs.org/internmap/-/internmap-2.0.3.tgz | ISC | ISC |
| katex | 0.16.47 | https://registry.npmjs.org/katex/-/katex-0.16.47.tgz | MIT | MIT |
| katex | 0.18.6 | https://registry.npmjs.org/katex/-/katex-0.18.6.tgz | MIT | MIT |
| khroma | 2.1.0 | https://registry.npmjs.org/khroma/-/khroma-2.1.0.tgz | See recorded evidence | MIT |
| layout-base | 1.0.2 | https://registry.npmjs.org/layout-base/-/layout-base-1.0.2.tgz | MIT | MIT |
| layout-base | 2.0.1 | https://registry.npmjs.org/layout-base/-/layout-base-2.0.1.tgz | MIT | MIT |
| lodash-es | 4.18.1 | https://registry.npmjs.org/lodash-es/-/lodash-es-4.18.1.tgz | MIT | MIT |
| lucide-react | 1.41.0 | https://registry.npmjs.org/lucide-react/-/lucide-react-1.41.0.tgz | ISC | ISC |
| marked | 16.4.2 | https://registry.npmjs.org/marked/-/marked-16.4.2.tgz | MIT | MIT |
| mermaid | 11.17.2 | https://registry.npmjs.org/mermaid/-/mermaid-11.17.2.tgz | MIT | MIT |
| package-manager-detector | 1.8.0 | https://registry.npmjs.org/package-manager-detector/-/package-manager-detector-1.8.0.tgz | MIT | MIT |
| path-data-parser | 0.1.0 | https://registry.npmjs.org/path-data-parser/-/path-data-parser-0.1.0.tgz | MIT | MIT |
| points-on-curve | 0.2.0 | https://registry.npmjs.org/points-on-curve/-/points-on-curve-0.2.0.tgz | MIT | MIT |
| points-on-path | 0.2.1 | https://registry.npmjs.org/points-on-path/-/points-on-path-0.2.1.tgz | MIT | MIT |
| react | 19.2.8 | https://registry.npmjs.org/react/-/react-19.2.8.tgz | MIT | MIT |
| react-dom | 19.2.8 | https://registry.npmjs.org/react-dom/-/react-dom-19.2.8.tgz | MIT | MIT |
| robust-predicates | 3.0.3 | https://registry.npmjs.org/robust-predicates/-/robust-predicates-3.0.3.tgz | Unlicense | Unlicense |
| roughjs | 4.6.6 | https://registry.npmjs.org/roughjs/-/roughjs-4.6.6.tgz | MIT | MIT |
| rw | 1.3.3 | https://registry.npmjs.org/rw/-/rw-1.3.3.tgz | BSD-3-Clause | BSD-3-Clause |
| safer-buffer | 2.1.2 | https://registry.npmjs.org/safer-buffer/-/safer-buffer-2.1.2.tgz | MIT | MIT |
| scheduler | 0.27.0 | https://registry.npmjs.org/scheduler/-/scheduler-0.27.0.tgz | MIT | MIT |
| strictdom | 1.0.1 | https://registry.npmjs.org/strictdom/-/strictdom-1.0.1.tgz | MIT | MIT |
| stylis | 4.4.0 | https://registry.npmjs.org/stylis/-/stylis-4.4.0.tgz | MIT | MIT |
| tailwind-merge | 3.6.0 | https://registry.npmjs.org/tailwind-merge/-/tailwind-merge-3.6.0.tgz | MIT | MIT |
| tinyexec | 1.3.1 | https://registry.npmjs.org/tinyexec/-/tinyexec-1.3.1.tgz | MIT | MIT |
| ts-dedent | 2.3.0 | https://registry.npmjs.org/ts-dedent/-/ts-dedent-2.3.0.tgz | MIT | MIT |
| uuid | 14.0.2 | https://registry.npmjs.org/uuid/-/uuid-14.0.2.tgz | MIT | MIT |

## Fonts

### ThGrotesk

ThGrotesk is a modified version of Hanken Grotesk, distributed under the SIL Open Font License, Version 1.1. Original design: Alfredo Marco Pradil (Hanken Grotesk); modifications: SilentPerson (font engineering and modification). Copyright 2021 The Hanken Grotesk Project Authors; modifications copyright 2026 SilentPerson. The license text is in `THIRD_PARTY_LICENSES/OFL-1.1-HankenGrotesk-ThGrotesk.txt`, distributed with the Software.

### HarmonyOS Sans SC

HarmonyOS Sans SC (Regular, Bold) is copyright 2021 Huawei Device Co., Ltd. and is used under the HarmonyOS Sans Fonts License Agreement. Yanbai states here that HarmonyOS Sans fonts are used, and this notice is repeated in the application’s about panel and in the installer. The license text is in `THIRD_PARTY_LICENSES/HarmonyOS-Sans-Fonts-License-Agreement.txt`, distributed with the Software.
