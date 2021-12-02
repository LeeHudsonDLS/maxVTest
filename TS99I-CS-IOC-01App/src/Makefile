TOP=../..

include $(TOP)/configure/CONFIG

# ------------------------
# Build an IOC Application
# ------------------------

PROD_IOC_vxWorks = TS99I-CS-IOC-01

# TS99I-CS-IOC-01.dbd will be installed into <top>/dbd
DBD += TS99I-CS-IOC-01.dbd

# TS99I-CS-IOC-01.dbd will be created from these files
TS99I-CS-IOC-01_DBD += base.dbd
TS99I-CS-IOC-01_DBD += calcSupport.dbd
TS99I-CS-IOC-01_DBD += stdSupport.dbd
TS99I-CS-IOC-01_DBD += genSubRecord.dbd
TS99I-CS-IOC-01_DBD += utility.dbd
TS99I-CS-IOC-01_DBD += drvIpac.dbd
TS99I-CS-IOC-01_DBD += Hy8001.dbd
TS99I-CS-IOC-01_DBD += Hy8401ip.dbd
TS99I-CS-IOC-01_DBD += Hy8403ip.dbd
TS99I-CS-IOC-01_DBD += DLS8515.dbd
TS99I-CS-IOC-01_DBD += DLS8512.dbd
TS99I-CS-IOC-01_DBD += asyn.dbd
TS99I-CS-IOC-01_DBD += drvAsynSerialPort.dbd
TS99I-CS-IOC-01_DBD += stream.dbd
TS99I-CS-IOC-01_DBD += FINS.dbd
TS99I-CS-IOC-01_DBD += motorSupport.dbd
TS99I-CS-IOC-01_DBD += devOms.dbd
TS99I-CS-IOC-01_DBD += as.dbd
TS99I-CS-IOC-01_DBD += asSupport.dbd
TS99I-CS-IOC-01_DBD += convert.dbd
TS99I-CS-IOC-01_DBD += asynRecord.dbd
TS99I-CS-IOC-01_DBD += busySupport.dbd
TS99I-CS-IOC-01_DBD += FERegistrar.dbd


TS99I-CS-IOC-01_DBD += mrfCommon.dbd
TS99I-CS-IOC-01_DBD += mrfEr.dbd
TS99I-CS-IOC-01_DBD += dlsTime.dbd

TS99I-CS-IOC-01_DBD += iocAdmin.dbd
TS99I-CS-IOC-01_DBD += devVxStats.dbd
TS99I-CS-IOC-01_DBD += IOCinfo.dbd

# ---------------------------------------------------------------------------------------------------
# TS99I-CS-IOC-01_registerRecordDeviceDriver.cpp will be created
# TS99I-CS-IOC-01.dbd
TS99I-CS-IOC-01_SRCS += TS99I-CS-IOC-01_registerRecordDeviceDriver.cpp

# These two lines are needed for non-vxWorks builds, such as Linux
TS99I-CS-IOC-01_SRCS_DEFAULT += TS99I-CS-IOC-01Main.cpp
TS99I-CS-IOC-01_SRCS_vxWorks += -nil-

# Add locally compiled object code
#TS99I-CS-IOC-01_SRCS +=

# The following adds object code from base/src/vxWorks
TS99I-CS-IOC-01_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# This line says that this IOC Application depends on the
# xxx Support Module
#TS99I-CS-IOC-01_LIBS += xxx

# This IOC Application depends on the following support modules
TS99I-CS-IOC-01_LIBS += DLS8515
TS99I-CS-IOC-01_LIBS += Hy8401ip
TS99I-CS-IOC-01_LIBS += Hy8403ip
TS99I-CS-IOC-01_LIBS += DLS8512
TS99I-CS-IOC-01_LIBS += utility
TS99I-CS-IOC-01_LIBS += Ipac
TS99I-CS-IOC-01_LIBS += oms
TS99I-CS-IOC-01_LIBS += motor
TS99I-CS-IOC-01_LIBS += genSub
TS99I-CS-IOC-01_LIBS += calc
TS99I-CS-IOC-01_LIBS += FELib
TS99I-CS-IOC-01_LIBS += PT100
TS99I-CS-IOC-01_LIBS += seq
TS99I-CS-IOC-01_LIBS += sscan
TS99I-CS-IOC-01_LIBS += pv
TS99I-CS-IOC-01_LIBS += std
TS99I-CS-IOC-01_LIBS += FINS
TS99I-CS-IOC-01_LIBS += stream
TS99I-CS-IOC-01_LIBS += asyn
TS99I-CS-IOC-01_LIBS += autosave
TS99I-CS-IOC-01_LIBS += busy
TS99I-CS-IOC-01_LIBS += pcre

TS99I-CS-IOC-01_LIBS += mrfCommon
TS99I-CS-IOC-01_LIBS += mrfEr
TS99I-CS-IOC-01_LIBS += dlsTime

TS99I-CS-IOC-01_LIBS += devIocStats
TS99I-CS-IOC-01_LIBS += IOCinfo

# We need to link this IOC Application against the EPICS Base libraries
TS99I-CS-IOC-01_LIBS += $(EPICS_BASE_IOC_LIBS)

# ---------------------------------------------------

# NOTE: To build SNL programs, SNCSEQ must be defined
# in the <top>/configure/RELEASE file
#
# The difference between a file with an "st" extension
# and one with an "stt" extension is:
# The "st" extension files get passed through the C preprocessor
# whereas the "stt" files do not.

#ifneq ($(SNCSEQ),)
    # This builds sncExample as a component of TS99I-CS-IOC-01
#    TS99I-CS-IOC-01_SNCFLAGS += +r
#    TS99I-CS-IOC-01_DBD      += sncExample.dbd
#    TS99I-CS-IOC-01_SRCS     += sncExample.stt
#    TS99I-CS-IOC-01_LIBS     += seq pv

    # The following builds sncExample as a standalone application
#    PROD_HOST           += sncExample
#    sncExample_SNCFLAGS += +m
#    sncExample_SRCS     += sncExample.stt
#    sncExample_LIBS     += seq pv
    # Here, we need to specify the dependency on EPICS Base libraries
    # again because this is a standalone application and
    # not part of TS99I-CS-IOC-01
#    sncExample_LIBS     += $(EPICS_BASE_HOST_LIBS)
#endif

include $(TOP)/configure/RULES

