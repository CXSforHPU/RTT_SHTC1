from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

if GetDepend("PKG_USING_SHTC1"):
    src += Glob('lib/shtc1.c')
    src += Glob('lib/sensirion_common.c')

if GetDepend("PKG_SHTC1_USING_SENSOR_V1"):
    src += Glob('sensor_sr_shtc1.c')
    src += Glob('sensirion_i2c.c')

# add lsm6dsl include path.
path  = [cwd, cwd + '/lib']

# add src and include to group.
group = DefineGroup('shtc1', src, depend = ['PKG_USING_SHTC1'], CPPPATH = path)

Return('group')
