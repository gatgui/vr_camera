import excons
import excons.tools.arnold as arnold

env = excons.MakeBaseEnv()

arch, maj, _, _ = arnold.Version(asString=False)

prefix = "arnold/%d.%d" % (arch, maj)

excons.DeclareTargets(env, [{"name": "VRCamera",
                             "type": "dynamicmodule",
                             "ext": arnold.PluginExt(),
                             "prefix": prefix,
                             "bldprefix": prefix,
                             "srcs": ["src/VRCamera.cpp"],
                             "custom": [arnold.Require],
                             "install": {prefix: ["src/VRCamera.mtd"],
                                         "maya": ["maya/aiVRCameraTemplate.py"]}}])