# FreeRDP: A Remote Desktop Protocol Implementation
# FreeRDP Servers
#
# Copyright 2012 Marc-Andre Moreau <marcandre.moreau@gmail.com>
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# Servers

add_subdirectory(common)

if(NOT WIN32)
	if(WITH_SAMPLE)
		add_subdirectory(Sample)
	endif()

	if(WITH_X11)
		add_subdirectory(X11)
	endif()

	if(APPLE AND (NOT IOS))
		add_subdirectory(Mac)
	endif()
else()
	add_subdirectory(Windows)
endif()

