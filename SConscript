from building import *
import os

cwd = GetCurrentDir()

path = [cwd]
src = ['system_at32f403a_407.c']

if rtconfig.PLATFORM in ['gcc', 'llvm-arm']:
    src += [os.path.join('startup', 'gcc', 'startup_at32f403a_407.s')]
elif rtconfig.PLATFORM in ['armcc', 'armclang']:
    src += [os.path.join('startup', 'mdk', 'startup_at32f403a_407.s')]
elif rtconfig.PLATFORM in ['iccarm']:
    src += [os.path.join('startup', 'iar', 'startup_at32f403a_407.s')]

group = DefineGroup('cmsis', src, depend = ['PKG_USING_AT32F403A_407_CMSIS_DRIVER'], CPPPATH = path)

Return('group')
