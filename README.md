使用方法
==============================================

載入JS

"
<script src="{TAG_FILE_ROOT}tinymce/tinymce.min.js" type="text/javascript"></script>
<script src="{TAG_FILE_ROOT}tinymce/config.js" type="text/javascript"></script>
<script>
	tiny_load({TAG_FILE_ROOT});
</script>
"

tiny_box 設定

$(function(){
	$(document).tiny_box({
		SWITCH : 1, // 0 => 全部 , 1 => 圖片 , 2 => 檔案
		ID : ".img_manage", // 綁定元素 (同css選取器)，可設定多個元素，使用 , 分隔
		ROOT : "{TAG_FILE_ROOT}" // 根目錄位置
	});
	
	$(document).tiny_box({
		SWITCH : 2, // 0 => 全部 , 1 => 圖片 , 2 => 檔案
		ID : ".file_manage", // 綁定元素 (同css選取器)，可設定多個元素，使用 , 分隔
		ROOT : "{TAG_FILE_ROOT}" // 根目錄位置
	});
	
	$(document).tiny_box({
		SWITCH : 0, // 0 => 全部 , 1 => 圖片 , 2 => 檔案
		ID : ".all_manage", // 綁定元素 (同css選取器)，可設定多個元素，使用 , 分隔
		ROOT : "{TAG_FILE_ROOT}" // 根目錄位置
	});
});


==============================================
tiny_box 使用範例
==============================================

圖檔選取器
<input type="text" id="p_img" name="p_s_pic" value="">
<input type="button" class="img_manage" name="btn" value="選擇圖檔" rel="p_img">

檔案選取器
<input type="text" id="fileid" name="file" value="">
<input type="button" class="file_manage" name="btn" value="選擇檔案" rel="fileid">
