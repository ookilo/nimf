---
layout: default
ref: index
lang: English
---

Nimf is an input method framework available for GNU / Linux. Nimf has a
module-based client-server architecture in which an application acts as a
client and communicates **synchronously** with the Nimf server via a
**Unix socket**.

## Lightweight

Nimf works as a **singleton mode** to reduce memory usage.
If necessary, Nimf can work as a multiple-instance mode.
The `nimf-daemon` handles both Nimf protocol and XIM protocol.

## Nimf provides:

* Input Method Server
  * `nimf-daemon`
* Language Engines
  * Chinese (alpha stage, based on sunpinyin, libchewing, librime)
  * Japanese (alpha stage, based on anthy)
  * Korean (based on libhangul)
* Service Modules
  * Indicator (based on appindicator)
  * Wayland
  * XIM (based on IMdkit)
* Client Modules
  * GTK+2, GTK+3, Qt4, Qt5
* Settings tool to configure the Nimf
  * `nimf-settings`
* Development files
  * C library and headers

## License

Nimf is free software: you can redistribute it and/or modify it
under the terms of the GNU Lesser General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

Nimf is distributed in the hope that it will be useful, but
**WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.**
See the GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with this program;  If not, see <http://www.gnu.org/licenses/>.
