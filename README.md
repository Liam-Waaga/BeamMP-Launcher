# BeamMP-Launcher
The launcher is the way we communitcate to outside the game, it does a few automated actions such as but not limited to: downloading the mod, launching the game, and create a connection to a server.


## This is a fork
This is a fork of [BeamMP-Launcher](https://github.com/BeamMP/BeamMP-Launcher). This fork is intended to add linux features which aren't present upstream. It may still work on windows, however linux is the primary focus.

## [Getting started](https://docs.beammp.com/game/getting-started/)

## Differences to Getting Started
Make sure you have the submodules populated. If not, run `git submodule init && git submodule update`
1. Run `./vcpkg/bootstrap-vcpkg.sh -disableMetrics` (add additional flags to suit your needs).
2. Run `cmake . -B build -DCMAKE_TOOLCHAIN_FILE=vcpkg/scripts/buildsystems/vcpkg.cmake -DVCPKG_TARGET_TRIPLET=x64-linux -G Ninja`.
3. Run ```cmake --build build -j `nproc` ```
4. Run `build/BeamMP-Launcher --help` to find which flags you want. Some reccomendations are `--no-launch` if running BeamNG through proton/wine, `--user-path <path>` for the same thing, and `--game-path <path>` if the game is in a different directory than provided by steam (ex. if it is in a library on another drive).

## License

BeamMP Launcher, a launcher for the BeamMP mod for BeamNG.drive
Copyright (C) 2024 BeamMP Ltd., BeamMP team and contributors.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
