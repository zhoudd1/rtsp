INCLUDE=-I./ -I../common -I../../include -I../../component/acodec -I../../extdrv/tw2865 -I../../extdrv/tlv320aic31 -I../../extdrv/ak7756en
LIBS=../../lib/libsns_ov4689.a ../../lib/libmpi.a ../../lib/libVoiceEngine.a ../../lib/libupvqe.a ../../lib/libdnvqe.a ../../lib/libisp.a ../../lib/lib_cmoscfg.a ../../lib/lib_iniparser.a ../../lib/lib_hiae.a ../../lib/lib_hiawb.a ../../lib/lib_hiaf.a ../../lib/lib_hidefog.a 
all:rtsp
rtsp:
	arm-hisiv300-linux-gcc  -g -o rtsp -Dhi3516a -DHICHIP=0x3516A100 -DSENSOR_TYPE=OMNIVISION_OV4689_MIPI_4M_30FPS -DHI_RELEASE -DHI_XXXX -lpthread -lm -ldl -DISP_V2 -DHI_ACODEC_TYPE_INNER -mcpu=cortex-a7 -mfloat-abi=softfp -mfpu=neon-vfpv4 -ffunction-sections -mno-unaligned-access -fno-aggressive-loop-optimizations -ldl  main.c rtspservice.c ringfifo.c rtputils.c rtsputils.c  ../common/sample_comm_sys.c ../common/sample_comm_vda.c ../common/sample_comm_audio.c ../common/sample_comm_isp.c ../common/sample_comm_vi.c ../common/sample_comm_vpss.c ../common/loadbmp.c ../common/sample_comm_ive.c ../common/sample_comm_vo.c ../common/sample_comm_venc.c $(INCLUDE) $(LIBS)
clean:
	rm -rfv rtsp
	
	
