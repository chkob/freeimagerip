SET(SRC ${3RDPARTY_DIR}/libwebp/src)

SET(SOURCE_FILES
	${SRC}/dec/alpha.c
	${SRC}/dec/buffer.c
	${SRC}/dec/frame.c
	${SRC}/dec/idec.c
	${SRC}/dec/io.c
	${SRC}/dec/quant.c
	${SRC}/dec/tree.c
	${SRC}/dec/vp8.c
	${SRC}/dec/vp8l.c
	${SRC}/dec/webp.c
	${SRC}/demux/anim_decode.c
	${SRC}/demux/demux.c
	${SRC}/dsp/alpha_processing.c
	${SRC}/dsp/alpha_processing_mips_dsp_r2.c
	${SRC}/dsp/alpha_processing_sse2.c
	${SRC}/dsp/alpha_processing_sse41.c
	${SRC}/dsp/argb.c
	${SRC}/dsp/argb_mips_dsp_r2.c
	${SRC}/dsp/argb_sse2.c
	${SRC}/dsp/cost.c
	${SRC}/dsp/cost_mips_dsp_r2.c
	${SRC}/dsp/cost_mips32.c
	${SRC}/dsp/cost_sse2.c
	${SRC}/dsp/cpu.c
	${SRC}/dsp/dec.c
	${SRC}/dsp/dec_clip_tables.c
	${SRC}/dsp/dec_mips32.c
	${SRC}/dsp/dec_mips_dsp_r2.c
	${SRC}/dsp/dec_msa.c
	${SRC}/dsp/dec_neon.c
	${SRC}/dsp/dec_sse2.c
	${SRC}/dsp/dec_sse41.c
	${SRC}/dsp/enc.c
	${SRC}/dsp/enc_avx2.c
	${SRC}/dsp/enc_mips_dsp_r2.c
	${SRC}/dsp/enc_mips32.c
	${SRC}/dsp/enc_neon.c
	${SRC}/dsp/enc_sse2.c
	${SRC}/dsp/enc_sse41.c
	${SRC}/dsp/filters.c
	${SRC}/dsp/filters_mips_dsp_r2.c
	${SRC}/dsp/filters_sse2.c
	${SRC}/dsp/lossless.c
	${SRC}/dsp/lossless_enc.c
	${SRC}/dsp/lossless_enc_mips32.c
	${SRC}/dsp/lossless_enc_neon.c
	${SRC}/dsp/lossless_enc_sse2.c
	${SRC}/dsp/lossless_enc_sse41.c
	${SRC}/dsp/lossless_mips_dsp_r2.c
	${SRC}/dsp/lossless_neon.c
	${SRC}/dsp/lossless_sse2.c
	${SRC}/dsp/rescaler.c
	${SRC}/dsp/rescaler_mips32.c
	${SRC}/dsp/rescaler_mips_dsp_r2.c
	${SRC}/dsp/rescaler_neon.c
	${SRC}/dsp/rescaler_sse2.c
	${SRC}/dsp/upsampling.c
	${SRC}/dsp/upsampling_mips_dsp_r2.c
	${SRC}/dsp/upsampling_neon.c
	${SRC}/dsp/upsampling_sse2.c
	${SRC}/dsp/yuv.c
	${SRC}/dsp/yuv_mips32.c
	${SRC}/dsp/yuv_mips_dsp_r2.c
	${SRC}/dsp/yuv_sse2.c
	${SRC}/enc/alpha.c
	${SRC}/enc/analysis.c
	${SRC}/enc/backward_references.c
	${SRC}/enc/config.c
	${SRC}/enc/cost.c
	${SRC}/enc/delta_palettization.c
	${SRC}/enc/filter.c
	${SRC}/enc/frame.c
	${SRC}/enc/histogram.c
	${SRC}/enc/iterator.c
	${SRC}/enc/near_lossless.c
	${SRC}/enc/picture.c
	${SRC}/enc/picture_csp.c
	${SRC}/enc/picture_psnr.c
	${SRC}/enc/picture_rescale.c
	${SRC}/enc/picture_tools.c
	${SRC}/enc/quant.c
	${SRC}/enc/syntax.c
	${SRC}/enc/token.c
	${SRC}/enc/tree.c
	${SRC}/enc/vp8l.c
	${SRC}/enc/webpenc.c
	${SRC}/mux/anim_encode.c
	${SRC}/mux/muxedit.c
	${SRC}/mux/muxinternal.c
	${SRC}/mux/muxread.c
	${SRC}/utils/bit_reader.c
	${SRC}/utils/bit_writer.c
	${SRC}/utils/color_cache.c
	${SRC}/utils/filters.c
	${SRC}/utils/huffman.c
	${SRC}/utils/huffman_encode.c
	${SRC}/utils/quant_levels.c
	${SRC}/utils/quant_levels_dec.c
	${SRC}/utils/random.c
	${SRC}/utils/rescaler.c
	${SRC}/utils/thread.c
	${SRC}/utils/utils.c
)

SOURCE_GROUP("Source Files" FILES ${SOURCE_FILES})

ADD_DEFINITIONS(-DWEBP_HAVE_AVX2 -DWEBP_USE_THREAD -DHAVE_WINCODEC_H)

ADD_LIBRARY(libwebp STATIC ${SOURCE_FILES})
