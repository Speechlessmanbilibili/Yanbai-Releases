# Third-Party Notices

Yanbai (砚白) incorporates the third-party components listed below. They are distributed in binary form as part of the Software and remain governed by their own license terms; nothing in the Yanbai End User License Agreement modifies or replaces those terms.

本文件列出随砚白以二进制形式分发的第三方组件，各组件仍适用其自身的许可条款，《砚白最终用户使用许可协议》不改变也不替代这些条款。

## How this list is built / 清单的生成方式

- Rust crates: the runtime dependency graph (cargo tree -e normal) for the four shipped targets (windows-msvc x64/arm64, linux-gnu x64/arm64). Build-time-only and other-platform crates are not listed.
- Frontend packages: the production dependency tree of frontend/package.json, excluding type-only packages (@types/*), which never reach the bundle.
- 中文：Rust 侧取四个交付目标（windows-msvc x64/arm64、linux-gnu x64/arm64）的运行时依赖图，只参与构建或只用于其他平台的包不在表内；前端取生产依赖树，纯类型包（@types/*）不列入，因为它们不会进入产物。

- Where a component offers a choice of licenses, the "Selected" column records the option the Licensor relies on. The rule is: split the SPDX expression on AND first (all branches are kept), then pick the highest-priority branch among the OR alternatives, in this order: MIT, Apache-2.0, Zlib, BSD-3-Clause, BSD-2-Clause, ISC, Unicode-3.0, Unlicense, MPL-2.0, LGPL-2.1-or-later.
- 中文：组件提供多种许可时，“Selected”列记载许可方适用的选项。规则是先按 AND 拆分（AND 的每一支都要遵守），再在 OR 的各支里按上述优先级取一项。

- Components under MPL-2.0 and LGPL are used unmodified; their source is available from the component's published distribution (crates.io or npm), which satisfies the source-availability obligations of those licenses.

## Rust crates (313)

| Component | Version | Licenses | Selected |
| --- | --- | --- | --- |
| adler2 | 2.0.1 | 0BSD OR MIT OR Apache-2.0 | MIT |
| aho-corasick | 1.1.5 | Unlicense OR MIT | MIT |
| alloc-no-stdlib | 2.0.4 | BSD-3-Clause | BSD-3-Clause |
| alloc-stdlib | 0.2.4 | BSD-3-Clause | BSD-3-Clause |
| anyhow | 1.0.104 | MIT OR Apache-2.0 | MIT |
| async-broadcast | 0.7.2 | MIT OR Apache-2.0 | MIT |
| async-channel | 2.5.0 | Apache-2.0 OR MIT | MIT |
| async-executor | 1.14.0 | Apache-2.0 OR MIT | MIT |
| async-io | 2.6.0 | Apache-2.0 OR MIT | MIT |
| async-lock | 3.4.2 | Apache-2.0 OR MIT | MIT |
| async-process | 2.5.0 | Apache-2.0 OR MIT | MIT |
| async-recursion | 1.1.1 (proc-macro) | MIT OR Apache-2.0 | MIT |
| async-signal | 0.2.14 | Apache-2.0 OR MIT | MIT |
| async-task | 4.7.1 | Apache-2.0 OR MIT | MIT |
| async-trait | 0.1.92 (proc-macro) | MIT OR Apache-2.0 | MIT |
| atk | 0.18.2 | MIT | MIT |
| atk-sys | 0.18.2 | MIT | MIT |
| atomic-waker | 1.1.2 | Apache-2.0 OR MIT | MIT |
| base64 | 0.22.1 | MIT OR Apache-2.0 | MIT |
| bit-set | 0.8.0 | Apache-2.0 OR MIT | MIT |
| bit-vec | 0.8.0 | Apache-2.0 OR MIT | MIT |
| bitflags | 2.13.1 | MIT OR Apache-2.0 | MIT |
| block-buffer | 0.10.4 | MIT OR Apache-2.0 | MIT |
| blocking | 1.7.0 | Apache-2.0 OR MIT | MIT |
| brotli | 8.0.4 | BSD-3-Clause AND MIT | BSD-3-Clause AND MIT |
| brotli-decompressor | 5.0.3 | BSD-3-Clause/MIT | BSD-3-Clause/MIT |
| bumpalo | 3.20.3 | MIT OR Apache-2.0 | MIT |
| byteorder | 1.5.0 | Unlicense OR MIT | MIT |
| bytes | 1.12.1 | MIT | MIT |
| cairo-rs | 0.18.5 | MIT | MIT |
| cairo-sys-rs | 0.18.2 | MIT | MIT |
| camino | 1.2.5 | MIT OR Apache-2.0 | MIT |
| cargo_metadata | 0.19.2 | MIT | MIT |
| cargo-platform | 0.1.9 | MIT OR Apache-2.0 | MIT |
| cfb | 0.7.3 | MIT | MIT |
| cfg-if | 1.0.4 | MIT OR Apache-2.0 | MIT |
| chardetng | 0.1.17 | Apache-2.0 OR MIT | MIT |
| concurrent-queue | 2.5.0 | Apache-2.0 OR MIT | MIT |
| cookie | 0.18.2 | MIT OR Apache-2.0 | MIT |
| core_detect | 1.0.0 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| cpufeatures | 0.2.17 | MIT OR Apache-2.0 | MIT |
| crc32fast | 1.5.1 | MIT OR Apache-2.0 | MIT |
| crossbeam-channel | 0.5.17 | MIT OR Apache-2.0 | MIT |
| crossbeam-utils | 0.8.23 | MIT OR Apache-2.0 | MIT |
| crypto-common | 0.1.7 | MIT OR Apache-2.0 | MIT |
| cssparser | 0.36.0 | MPL-2.0 | MPL-2.0 |
| cssparser-macros | 0.6.1 (proc-macro) | MPL-2.0 | MPL-2.0 |
| ctor | 0.8.0 | Apache-2.0 OR MIT | MIT |
| ctor-proc-macro | 0.0.7 (proc-macro) | Apache-2.0 OR MIT | MIT |
| darling | 0.23.0 | MIT | MIT |
| darling_core | 0.23.0 | MIT | MIT |
| darling_macro | 0.23.0 (proc-macro) | MIT | MIT |
| dbus | 0.9.12 | Apache-2.0/MIT | Apache-2.0/MIT |
| deranged | 0.5.8 | MIT OR Apache-2.0 | MIT |
| derive_more | 2.1.1 | MIT | MIT |
| derive_more-impl | 2.1.1 (proc-macro) | MIT | MIT |
| digest | 0.10.7 | MIT OR Apache-2.0 | MIT |
| dirs | 6.0.0 | MIT OR Apache-2.0 | MIT |
| dirs-sys | 0.5.0 | MIT OR Apache-2.0 | MIT |
| displaydoc | 0.2.7 (proc-macro) | MIT OR Apache-2.0 | MIT |
| dlopen2 | 0.8.2 | MIT | MIT |
| dlopen2_derive | 0.4.3 (proc-macro) | MIT | MIT |
| dom_query | 0.27.0 | MIT | MIT |
| dpi | 0.1.2 | Apache-2.0 AND MIT | Apache-2.0 AND MIT |
| dtoa | 1.0.11 | MIT OR Apache-2.0 | MIT |
| dtoa-short | 0.3.5 | MPL-2.0 | MPL-2.0 |
| dunce | 1.0.5 | CC0-1.0 OR MIT-0 OR Apache-2.0 | Apache-2.0 |
| dyn-clone | 1.0.20 | MIT OR Apache-2.0 | MIT |
| encoding_rs | 0.8.40 | (Apache-2.0 OR MIT) AND BSD-3-Clause | MIT AND BSD-3-Clause |
| endi | 1.1.1 | MIT | MIT |
| enumflags2 | 0.7.12 | MIT OR Apache-2.0 | MIT |
| enumflags2_derive | 0.7.12 (proc-macro) | MIT OR Apache-2.0 | MIT |
| equivalent | 1.0.2 | Apache-2.0 OR MIT | MIT |
| erased-serde | 0.4.10 | MIT OR Apache-2.0 | MIT |
| errno | 0.3.14 | MIT OR Apache-2.0 | MIT |
| event-listener | 5.4.2 | Apache-2.0 OR MIT | MIT |
| event-listener-strategy | 0.5.4 | Apache-2.0 OR MIT | MIT |
| fastrand | 2.5.0 | Apache-2.0 OR MIT | MIT |
| fdeflate | 0.3.7 | MIT OR Apache-2.0 | MIT |
| fern | 0.7.1 | MIT | MIT |
| field-offset | 0.3.6 | MIT OR Apache-2.0 | MIT |
| flate2 | 1.1.10 | MIT OR Apache-2.0 | MIT |
| fnv | 1.0.7 | Apache-2.0 / MIT | MIT |
| foldhash | 0.2.0 | Zlib | Zlib |
| form_urlencoded | 1.2.2 | MIT OR Apache-2.0 | MIT |
| futures-channel | 0.3.34 | MIT OR Apache-2.0 | MIT |
| futures-core | 0.3.34 | MIT OR Apache-2.0 | MIT |
| futures-executor | 0.3.34 | MIT OR Apache-2.0 | MIT |
| futures-io | 0.3.34 | MIT OR Apache-2.0 | MIT |
| futures-lite | 2.6.1 | Apache-2.0 OR MIT | MIT |
| futures-macro | 0.3.34 (proc-macro) | MIT OR Apache-2.0 | MIT |
| futures-task | 0.3.34 | MIT OR Apache-2.0 | MIT |
| futures-util | 0.3.34 | MIT OR Apache-2.0 | MIT |
| gdk | 0.18.2 | MIT | MIT |
| gdk-pixbuf | 0.18.5 | MIT | MIT |
| gdk-pixbuf-sys | 0.18.0 | MIT | MIT |
| gdk-sys | 0.18.2 | MIT | MIT |
| gdkwayland-sys | 0.18.2 | MIT | MIT |
| gdkx11 | 0.18.2 | MIT | MIT |
| gdkx11-sys | 0.18.2 | MIT | MIT |
| generic-array | 0.14.7 | MIT | MIT |
| getrandom | 0.3.4 | MIT OR Apache-2.0 | MIT |
| gio | 0.18.4 | MIT | MIT |
| gio-sys | 0.18.1 | MIT | MIT |
| glib | 0.18.5 | MIT | MIT |
| glib-macros | 0.18.5 (proc-macro) | MIT | MIT |
| glib-sys | 0.18.1 | MIT | MIT |
| glob | 0.3.4 | MIT OR Apache-2.0 | MIT |
| gobject-sys | 0.18.0 | MIT | MIT |
| gtk | 0.18.2 | MIT | MIT |
| gtk-sys | 0.18.2 | MIT | MIT |
| gtk3-macros | 0.18.2 (proc-macro) | MIT | MIT |
| hashbrown | 0.17.1 | MIT OR Apache-2.0 | MIT |
| heck | 0.5.0 | MIT OR Apache-2.0 | MIT |
| hex | 0.4.3 | MIT OR Apache-2.0 | MIT |
| html5ever | 0.38.0 | MIT OR Apache-2.0 | MIT |
| http | 1.5.0 | MIT OR Apache-2.0 | MIT |
| ico | 0.5.0 | MIT | MIT |
| icu_collections | 2.3.0 | Unicode-3.0 | Unicode-3.0 |
| icu_locale_core | 2.3.0 | Unicode-3.0 | Unicode-3.0 |
| icu_normalizer | 2.3.0 | Unicode-3.0 | Unicode-3.0 |
| icu_normalizer_data | 2.3.0 | Unicode-3.0 | Unicode-3.0 |
| icu_properties | 2.3.0 | Unicode-3.0 | Unicode-3.0 |
| icu_properties_data | 2.3.0 | Unicode-3.0 | Unicode-3.0 |
| icu_provider | 2.3.1 | Unicode-3.0 | Unicode-3.0 |
| ident_case | 1.0.1 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| idna | 1.1.0 | MIT OR Apache-2.0 | MIT |
| idna_adapter | 1.2.2 | Apache-2.0 OR MIT | MIT |
| indexmap | 2.14.2 | Apache-2.0 OR MIT | MIT |
| infer | 0.19.0 | MIT | MIT |
| itoa | 1.0.18 | MIT OR Apache-2.0 | MIT |
| javascriptcore-rs | 1.1.2 | MIT | MIT |
| javascriptcore-rs-sys | 1.1.1 | MIT | MIT |
| json-patch | 3.0.1 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| jsonptr | 0.6.3 | MIT OR Apache-2.0 | MIT |
| keyboard-types | 0.7.0 | MIT OR Apache-2.0 | MIT |
| libc | 0.2.189 | MIT OR Apache-2.0 | MIT |
| libdbus-sys | 0.2.7 | Apache-2.0/MIT | Apache-2.0/MIT |
| linux-raw-sys | 0.12.1 | Apache-2.0 WITH LLVM-exception OR Apache-2.0 OR MIT | MIT |
| litemap | 0.8.3 | Unicode-3.0 | Unicode-3.0 |
| lock_api | 0.4.14 | MIT OR Apache-2.0 | MIT |
| log | 0.4.34 | MIT OR Apache-2.0 | MIT |
| markup5ever | 0.38.0 | MIT OR Apache-2.0 | MIT |
| memchr | 2.8.3 | Unlicense OR MIT | MIT |
| memoffset | 0.9.1 | MIT | MIT |
| mime | 0.3.17 | MIT OR Apache-2.0 | MIT |
| miniz_oxide | 0.9.1 | MIT OR Zlib OR Apache-2.0 | MIT |
| mio | 1.2.3 | MIT | MIT |
| muda | 0.19.3 | Apache-2.0 OR MIT | MIT |
| multiversion | 0.8.0 | MIT OR Apache-2.0 | MIT |
| multiversion_no_op | 1.0.0 (proc-macro) | Apache-2.0 OR MIT | MIT |
| multiversion-macros | 0.8.0 (proc-macro) | MIT OR Apache-2.0 | MIT |
| new_debug_unreachable | 1.0.6 | MIT | MIT |
| num_threads | 0.1.7 | MIT OR Apache-2.0 | MIT |
| num-conv | 0.2.2 | MIT OR Apache-2.0 | MIT |
| once_cell | 1.21.4 | MIT OR Apache-2.0 | MIT |
| option-ext | 0.2.0 | MPL-2.0 | MPL-2.0 |
| ordered-stream | 0.2.0 | MIT OR Apache-2.0 | MIT |
| pango | 0.18.3 | MIT | MIT |
| pango-sys | 0.18.0 | MIT | MIT |
| parking | 2.2.1 | Apache-2.0 OR MIT | MIT |
| parking_lot | 0.12.5 | MIT OR Apache-2.0 | MIT |
| parking_lot_core | 0.9.12 | MIT OR Apache-2.0 | MIT |
| percent-encoding | 2.3.2 | MIT OR Apache-2.0 | MIT |
| phf | 0.13.1 | MIT | MIT |
| phf_generator | 0.13.1 | MIT | MIT |
| phf_macros | 0.13.1 (proc-macro) | MIT | MIT |
| phf_shared | 0.13.1 | MIT | MIT |
| pin-project-lite | 0.2.17 | Apache-2.0 OR MIT | MIT |
| piper | 0.2.5 | MIT OR Apache-2.0 | MIT |
| plist | 1.10.1 | MIT | MIT |
| png | 0.17.16 | MIT OR Apache-2.0 | MIT |
| polling | 3.11.0 | Apache-2.0 OR MIT | MIT |
| potential_utf | 0.1.6 | Unicode-3.0 | Unicode-3.0 |
| powerfmt | 0.2.0 | MIT OR Apache-2.0 | MIT |
| precomputed-hash | 0.1.1 | MIT | MIT |
| proc-macro-crate | 2.0.2 | MIT OR Apache-2.0 | MIT |
| proc-macro-error | 1.0.4 | MIT OR Apache-2.0 | MIT |
| proc-macro-error-attr | 1.0.4 (proc-macro) | MIT OR Apache-2.0 | MIT |
| proc-macro2 | 1.0.107 | MIT OR Apache-2.0 | MIT |
| quick-xml | 0.42.0 | MIT | MIT |
| quote | 1.0.47 | MIT OR Apache-2.0 | MIT |
| raw-window-handle | 0.6.2 | MIT OR Apache-2.0 OR Zlib | MIT |
| regex | 1.13.1 | MIT OR Apache-2.0 | MIT |
| regex-automata | 0.4.18 | MIT OR Apache-2.0 | MIT |
| regex-syntax | 0.8.11 | MIT OR Apache-2.0 | MIT |
| rfd | 0.16.0 | MIT | MIT |
| roxmltree | 0.21.1 | MIT OR Apache-2.0 | MIT |
| rustc-hash | 2.1.3 | Apache-2.0 OR MIT | MIT |
| rustix | 1.1.4 | Apache-2.0 WITH LLVM-exception OR Apache-2.0 OR MIT | MIT |
| same-file | 1.0.6 | Unlicense/MIT | Unlicense/MIT |
| schemars | 0.8.22 | MIT | MIT |
| schemars_derive | 0.8.22 (proc-macro) | MIT | MIT |
| scopeguard | 1.2.0 | MIT OR Apache-2.0 | MIT |
| selectors | 0.36.1 | MPL-2.0 | MPL-2.0 |
| semver | 1.0.28 | MIT OR Apache-2.0 | MIT |
| serde | 1.0.229 | MIT OR Apache-2.0 | MIT |
| serde_core | 1.0.229 | MIT OR Apache-2.0 | MIT |
| serde_derive | 1.0.229 (proc-macro) | MIT OR Apache-2.0 | MIT |
| serde_derive_internals | 0.29.1 | MIT OR Apache-2.0 | MIT |
| serde_json | 1.0.151 | MIT OR Apache-2.0 | MIT |
| serde_repr | 0.1.21 (proc-macro) | MIT OR Apache-2.0 | MIT |
| serde_spanned | 1.1.1 | MIT OR Apache-2.0 | MIT |
| serde_with | 3.22.0 | MIT OR Apache-2.0 | MIT |
| serde_with_macros | 3.22.0 (proc-macro) | MIT OR Apache-2.0 | MIT |
| serde-untagged | 0.1.9 | MIT OR Apache-2.0 | MIT |
| serialize-to-javascript | 0.1.2 | MIT OR Apache-2.0 | MIT |
| serialize-to-javascript-impl | 0.1.2 (proc-macro) | MIT OR Apache-2.0 | MIT |
| servo_arc | 0.4.3 | MIT OR Apache-2.0 | MIT |
| sha2 | 0.10.9 | MIT OR Apache-2.0 | MIT |
| signal-hook-registry | 1.4.8 | MIT OR Apache-2.0 | MIT |
| simd-adler32 | 0.3.10 | MIT | MIT |
| simdutf8 | 0.1.5 | MIT OR Apache-2.0 | MIT |
| siphasher | 1.0.3 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| slab | 0.4.12 | MIT | MIT |
| smallvec | 1.16.0 | MIT OR Apache-2.0 | MIT |
| socket2 | 0.6.5 | MIT OR Apache-2.0 | MIT |
| softbuffer | 0.4.8 | MIT OR Apache-2.0 | MIT |
| soup3 | 0.5.0 | MIT | MIT |
| soup3-sys | 0.5.0 | MIT | MIT |
| stable_deref_trait | 1.2.1 | MIT OR Apache-2.0 | MIT |
| string_cache | 0.9.0 | MIT OR Apache-2.0 | MIT |
| strsim | 0.11.1 | MIT | MIT |
| syn | 3.0.5 | MIT OR Apache-2.0 | MIT |
| synstructure | 0.13.2 | MIT | MIT |
| tao | 0.35.3 | Apache-2.0 | Apache-2.0 |
| target-features | 0.1.6 | MIT OR Apache-2.0 | MIT |
| tauri | 2.11.5 | Apache-2.0 OR MIT | MIT |
| tauri-codegen | 2.6.3 | Apache-2.0 OR MIT | MIT |
| tauri-macros | 2.6.3 (proc-macro) | Apache-2.0 OR MIT | MIT |
| tauri-plugin-dialog | 2.7.3 | Apache-2.0 OR MIT | MIT |
| tauri-plugin-fs | 2.5.2 | Apache-2.0 OR MIT | MIT |
| tauri-plugin-log | 2.9.1 | Apache-2.0 OR MIT | MIT |
| tauri-plugin-single-instance | 2.4.4 | Apache-2.0 OR MIT | MIT |
| tauri-runtime | 2.11.3 | Apache-2.0 OR MIT | MIT |
| tauri-runtime-wry | 2.11.4 | Apache-2.0 OR MIT | MIT |
| tauri-utils | 2.9.3 | Apache-2.0 OR MIT | MIT |
| tendril | 0.5.1 | MIT OR Apache-2.0 | MIT |
| thiserror | 2.0.20 | MIT OR Apache-2.0 | MIT |
| thiserror-impl | 2.0.20 (proc-macro) | MIT OR Apache-2.0 | MIT |
| time | 0.3.55 | MIT OR Apache-2.0 | MIT |
| time-core | 0.1.9 | MIT OR Apache-2.0 | MIT |
| time-macros | 0.2.32 (proc-macro) | MIT OR Apache-2.0 | MIT |
| tinystr | 0.8.4 | Unicode-3.0 | Unicode-3.0 |
| tokio | 1.53.1 | MIT | MIT |
| toml | 1.1.5+spec-1.1.0 | MIT OR Apache-2.0 | MIT |
| toml_datetime | 1.1.1+spec-1.1.0 | MIT OR Apache-2.0 | MIT |
| toml_edit | 0.20.2 | MIT OR Apache-2.0 | MIT |
| toml_parser | 1.1.3+spec-1.1.0 | MIT OR Apache-2.0 | MIT |
| toml_writer | 1.1.2+spec-1.1.0 | MIT OR Apache-2.0 | MIT |
| tracing | 0.1.44 | MIT | MIT |
| tracing-attributes | 0.1.31 (proc-macro) | MIT | MIT |
| tracing-core | 0.1.36 | MIT | MIT |
| typeid | 1.0.3 | MIT OR Apache-2.0 | MIT |
| typenum | 1.20.1 | MIT OR Apache-2.0 | MIT |
| unic-char-property | 0.9.0 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| unic-char-range | 0.9.0 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| unic-common | 0.9.0 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| unic-ucd-ident | 0.9.0 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| unic-ucd-version | 0.9.0 | MIT/Apache-2.0 | MIT/Apache-2.0 |
| unicode-ident | 1.0.24 | (MIT OR Apache-2.0) AND Unicode-3.0 | MIT AND Unicode-3.0 |
| unicode-segmentation | 1.13.3 | MIT OR Apache-2.0 | MIT |
| url | 2.5.8 | MIT OR Apache-2.0 | MIT |
| urlpattern | 0.3.0 | MIT | MIT |
| utf8_iter | 1.0.4 | Apache-2.0 OR MIT | MIT |
| uuid | 1.26.0 | Apache-2.0 OR MIT | MIT |
| walkdir | 2.5.0 | Unlicense/MIT | Unlicense/MIT |
| web_atoms | 0.2.6 | MIT OR Apache-2.0 | MIT |
| webkit2gtk | 2.0.2 | MIT | MIT |
| webkit2gtk-sys | 2.0.2 | MIT | MIT |
| webview2-com | 0.38.2 | MIT | MIT |
| webview2-com-macros | 0.8.1 (proc-macro) | MIT | MIT |
| webview2-com-sys | 0.38.2 | MIT | MIT |
| winapi-util | 0.1.11 | Unlicense OR MIT | MIT |
| window-vibrancy | 0.6.0 | Apache-2.0 OR MIT | MIT |
| windows | 0.61.3 | MIT OR Apache-2.0 | MIT |
| windows_aarch64_msvc | 0.52.6 | MIT OR Apache-2.0 | MIT |
| windows_x86_64_msvc | 0.52.6 | MIT OR Apache-2.0 | MIT |
| windows-collections | 0.2.0 | MIT OR Apache-2.0 | MIT |
| windows-core | 0.61.2 | MIT OR Apache-2.0 | MIT |
| windows-future | 0.2.1 | MIT OR Apache-2.0 | MIT |
| windows-implement | 0.60.2 (proc-macro) | MIT OR Apache-2.0 | MIT |
| windows-interface | 0.59.3 (proc-macro) | MIT OR Apache-2.0 | MIT |
| windows-link | 0.2.1 | MIT OR Apache-2.0 | MIT |
| windows-numerics | 0.2.0 | MIT OR Apache-2.0 | MIT |
| windows-result | 0.3.4 | MIT OR Apache-2.0 | MIT |
| windows-strings | 0.4.2 | MIT OR Apache-2.0 | MIT |
| windows-sys | 0.61.2 | MIT OR Apache-2.0 | MIT |
| windows-targets | 0.52.6 | MIT OR Apache-2.0 | MIT |
| windows-threading | 0.1.0 | MIT OR Apache-2.0 | MIT |
| windows-version | 0.1.7 | MIT OR Apache-2.0 | MIT |
| winnow | 1.0.4 | MIT | MIT |
| writeable | 0.6.4 | Unicode-3.0 | Unicode-3.0 |
| wry | 0.55.1 | Apache-2.0 OR MIT | MIT |
| x11 | 2.21.0 | MIT | MIT |
| x11-dl | 2.21.0 | MIT | MIT |
| yoke | 0.8.3 | Unicode-3.0 | Unicode-3.0 |
| yoke-derive | 0.8.2 (proc-macro) | Unicode-3.0 | Unicode-3.0 |
| zbus | 5.19.0 | MIT | MIT |
| zbus_macros | 5.19.0 (proc-macro) | MIT | MIT |
| zbus_names | 4.3.4 | MIT | MIT |
| zcheapstr | 1.1.0 | MIT | MIT |
| zerofrom | 0.1.8 | Unicode-3.0 | Unicode-3.0 |
| zerofrom-derive | 0.1.7 (proc-macro) | Unicode-3.0 | Unicode-3.0 |
| zerotrie | 0.2.5 | Unicode-3.0 | Unicode-3.0 |
| zerovec | 0.11.8 | Unicode-3.0 | Unicode-3.0 |
| zerovec-derive | 0.11.6 (proc-macro) | Unicode-3.0 | Unicode-3.0 |
| zip | 2.4.2 | MIT | MIT |
| zmij | 1.0.23 | MIT | MIT |
| zopfli | 0.8.3 | Apache-2.0 | Apache-2.0 |
| zvariant | 5.15.0 | MIT | MIT |
| zvariant_derive | 5.15.0 (proc-macro) | MIT | MIT |
| zvariant_utils | 4.2.0 | MIT | MIT |

## Frontend packages (82)

| Component | Version | Licenses | Selected |
| --- | --- | --- | --- |
| @antfu/install-pkg | 2.0.1 | MIT | MIT |
| @braintree/sanitize-url | 7.1.2 | MIT | MIT |
| @chevrotain/types | 11.1.2 | Apache-2.0 | Apache-2.0 |
| @iconify/types | 2.0.0 | MIT | MIT |
| @iconify/utils | 3.1.6 | MIT | MIT |
| @mermaid-js/parser | 1.2.1 | MIT | MIT |
| @tauri-apps/api | 2.11.1 | Apache-2.0 OR MIT | MIT |
| @tauri-apps/plugin-dialog | 2.7.3 | MIT OR Apache-2.0 | MIT |
| @tauri-apps/plugin-fs | 2.5.2 | MIT OR Apache-2.0 | MIT |
| @upsetjs/venn.js | 2.0.0 | MIT | MIT |
| clsx | 2.1.1 | MIT | MIT |
| commander | 15.0.0 | MIT | MIT |
| cose-base | 1.0.3 | MIT | MIT |
| cytoscape | 3.34.2 | MIT | MIT |
| cytoscape-cose-bilkent | 4.1.0 | MIT | MIT |
| cytoscape-fcose | 2.2.0 | MIT | MIT |
| d3 | 7.9.0 | ISC | ISC |
| d3-array | 3.2.4 | ISC | ISC |
| d3-axis | 3.0.0 | ISC | ISC |
| d3-brush | 3.0.0 | ISC | ISC |
| d3-chord | 3.0.1 | ISC | ISC |
| d3-color | 3.1.0 | ISC | ISC |
| d3-contour | 4.0.2 | ISC | ISC |
| d3-delaunay | 6.0.4 | ISC | ISC |
| d3-dispatch | 3.0.1 | ISC | ISC |
| d3-drag | 3.0.0 | ISC | ISC |
| d3-dsv | 3.0.1 | ISC | ISC |
| d3-ease | 3.0.1 | BSD-3-Clause | BSD-3-Clause |
| d3-fetch | 3.0.1 | ISC | ISC |
| d3-force | 3.0.0 | ISC | ISC |
| d3-format | 3.1.2 | ISC | ISC |
| d3-geo | 3.1.1 | ISC | ISC |
| d3-hierarchy | 3.1.2 | ISC | ISC |
| d3-interpolate | 3.0.1 | ISC | ISC |
| d3-path | 3.1.0 | ISC | ISC |
| d3-polygon | 3.0.1 | ISC | ISC |
| d3-quadtree | 3.0.1 | ISC | ISC |
| d3-random | 3.0.1 | ISC | ISC |
| d3-sankey | 0.12.3 | BSD-3-Clause | BSD-3-Clause |
| d3-scale | 4.0.2 | ISC | ISC |
| d3-scale-chromatic | 3.1.0 | ISC | ISC |
| d3-selection | 3.0.0 | ISC | ISC |
| d3-shape | 3.2.0 | ISC | ISC |
| d3-time | 3.1.0 | ISC | ISC |
| d3-time-format | 4.1.0 | ISC | ISC |
| d3-timer | 3.0.1 | ISC | ISC |
| d3-transition | 3.0.1 | ISC | ISC |
| d3-zoom | 3.0.0 | ISC | ISC |
| dagre-d3-es | 7.0.14 | MIT | MIT |
| dayjs | 1.11.23 | MIT | MIT |
| delaunator | 5.1.0 | ISC | ISC |
| dompurify | 3.4.15 | (MPL-2.0 OR Apache-2.0) | Apache-2.0 |
| es-toolkit | 1.52.0 | MIT | MIT |
| fastdom | 1.0.12 | MIT | MIT |
| hachure-fill | 0.5.2 | MIT | MIT |
| iconv-lite | 0.6.3 | MIT | MIT |
| import-meta-resolve | 4.2.0 | MIT | MIT |
| internmap | 2.0.3 | ISC | ISC |
| katex | 0.18.6 | MIT | MIT |
| khroma | 2.1.0 |  | 见组件自身分发 |
| layout-base | 1.0.2 | MIT | MIT |
| lodash-es | 4.18.1 | MIT | MIT |
| lucide-react | 1.41.0 | ISC | ISC |
| marked | 16.4.2 | MIT | MIT |
| mermaid | 11.17.2 | MIT | MIT |
| package-manager-detector | 1.8.0 | MIT | MIT |
| path-data-parser | 0.1.0 | MIT | MIT |
| points-on-curve | 0.2.0 | MIT | MIT |
| points-on-path | 0.2.1 | MIT | MIT |
| react | 19.2.8 | MIT | MIT |
| react-dom | 19.2.8 | MIT | MIT |
| robust-predicates | 3.0.3 | Unlicense | Unlicense |
| roughjs | 4.6.6 | MIT | MIT |
| rw | 1.3.3 | BSD-3-Clause | BSD-3-Clause |
| safer-buffer | 2.1.2 | MIT | MIT |
| scheduler | 0.27.0 | MIT | MIT |
| strictdom | 1.0.1 | MIT | MIT |
| stylis | 4.4.0 | MIT | MIT |
| tailwind-merge | 3.6.0 | MIT | MIT |
| tinyexec | 1.3.1 | MIT | MIT |
| ts-dedent | 2.3.0 | MIT | MIT |
| uuid | 14.0.2 | MIT | MIT |

## Fonts

### ThGrotesk

ThGrotesk is a modified version of Hanken Grotesk, distributed under the SIL Open Font License, Version 1.1. Original design: Alfredo Marco Pradil (Hanken Grotesk); modifications: SilentPerson (font engineering and modification). Copyright 2021 The Hanken Grotesk Project Authors; modifications copyright 2026 SilentPerson. The license text is in `THIRD_PARTY_LICENSES/OFL-1.1-HankenGrotesk-ThGrotesk.txt`, distributed with the Software.

### HarmonyOS Sans SC

HarmonyOS Sans SC (Regular, Bold) is copyright 2021 Huawei Device Co., Ltd. and is used under the HarmonyOS Sans Fonts License Agreement. Yanbai states here that HarmonyOS Sans fonts are used, and this notice is repeated in the application's about panel and in the installer. The license text is in `THIRD_PARTY_LICENSES/HarmonyOS-Sans-Fonts-License-Agreement.txt`, distributed with the Software.

