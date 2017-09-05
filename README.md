Bu basit fonksiyon bir HTML formunda zorunlu olarak belirlediğiniz veri giriş alanlarını tarayarak hemen üstündeki label'ın sonuna (*) ifadesi ekler.
<br><br>
<b>Önemli Uyarı:</b> Label'ın sonuna ekleme yapabilmesi için label'ın "for" niteliği ile input'un "id" niteliği eşleşmelidir.
<br>
<br>
<br>
<br>
<br>

	<div class="container">
		<h1>Add Star to Required Input's Labels</h1>
		<p></p>
		<br><hr><br>
		<form id="affilates_request_form" action="">
			<div class="row">
				<div class="col-md-6">
					<div class="panel panel-default">
						<div class="panel-heading">
							Şirket Bilgileri
						</div>
						<div class="panel-body">
							<div class="form-group">
								<label for="company_name">Şirket Adı</label>
								<input class="form-control" name="company_name" id="company_name" type="text" required="">
							</div>
							<div class="form-group">
								<label for="tax_office">Vergi Dairesi</label>
								<input class="form-control" name="tax_office" id="tax_office" type="text" required="">
							</div>
							<div class="form-group">
								<label for="tax_number">Vergi Numarası</label>
								<input class="form-control" name="tax_number" id="tax_number" type="text" required="">
							</div>
							<div class="form-group">
								<label for="sector">Sektör</label>
								<input class="form-control" name="sector" id="sector" type="text" required="">
							</div>
							<hr>
							<div class="form-group">
								<label for="city">Şehir</label>
								<input class="form-control" name="city" id="city" type="text" required="">
							</div>
							<div class="form-group">
								<label for="county">İlçe</label>
								<input class="form-control" name="county" id="county" type="text" required="">
							</div>
							<div class="form-group">
								<label for="address">Adres</label>
								<input class="form-control" name="address" id="address" type="text" required="">
							</div>
							<div class="form-group">
								<label for="postcode">Posta Kodu</label>
								<input class="form-control" name="postcode" id="postcode" type="text" required="">
							</div>
							<hr>
							<div class="form-group">
								<label for="phone">Telefon</label>
								<input class="form-control" name="phone" id="phone" type="text" required="">
							</div>
							<div class="form-group">
								<label for="email">E-Mail Adresi</label>
								<input class="form-control" name="email" id="email" type="text" required="">
							</div>
							<div class="form-group">
								<label for="website">Website</label>
								<input class="form-control" name="website" id="website" type="text">
							</div>
						</div>
					</div>
				</div>
				<div class="col-md-6">
					<div class="panel panel-default">
						<div class="panel-heading">
							Yetkili Bilgileri
						</div>
						<div class="panel-body">
							<div class="form-group">
								<label for="authorized_first_name">Yetkili Adı</label>
								<input class="form-control" name="authorized_first_name" id="authorized_first_name" type="text" required="">
							</div>
							<div class="form-group">
								<label for="authorized_last_name">Yetkili Soyadı</label>
								<input class="form-control" name="authorized_last_name" id="authorized_last_name" type="text" required="">
							</div>
							<div class="form-group">
								<label for="authorized_email">Yetkili E-Postası</label>
								<input class="form-control" name="authorized_email" id="authorized_email" type="text" required="">
							</div>
							<div class="form-group">
								<label for="authorized_phone1">Yetkili Telefon - 1</label>
								<input class="form-control" name="authorized_phone1" id="authorized_phone1" type="text" required="">
							</div>
							<div class="form-group">
								<label for="authorized_phone2">Yetkili Telefon - 2</label>
								<input class="form-control" name="authorized_phone2" id="authorized_phone2" type="text">
							</div>
						</div>
					</div>
					<br>
					<div class="panel panel-default">
						<div class="panel-heading">
							Diğer Gerekli Bilgiler
						</div>
						<div class="panel-body">
							<div class="form-group">
								<label for="survey">Bizi Hangi Kanaldan Buldunuz?</label>
								<select class="form-control" name="survey" id="survey" required="">
									<option value="0">İnternetten</option>
								</select>
							</div>
							<div class="form-group">
								<label for="partner_type">Hangi İş Ortaklığı Türlerini Düşünüyorsunuz?</label>
								<select class="form-control" name="partner_type" id="partner_type" multiple="" required="">
									<option value="1">Sanal Sunucu Satışı</option>
									<option value="2">Fiziksel Sunucu Satışı</option>
									<option value="3">Web Hosting Satışı</option>
									<option value="4">Domain Satışı</option>
									<option value="5">Diğer</option>
								</select>
							</div>
							<div class="form-group">
								<label for="sales_target">Aylık Satış Hedefiniz (Adet Olarak)</label>
								<input class="form-control" name="sales_target" id="sales_target" type="number" required="" min="0">
							</div>
						</div>
					</div>
					<div class="form-group1 text-right">
						<button class="btn btn-success">
							Başvuruyu Tamamla <i class="fa fa-fw fa-paper-plane"></i>
						</button>
					</div>
				</div>
			</div>
		</form>
	</div>

	<script>
		$(':input[required]').each(function() { // Zorunlu niteliğine sahip bütün alanları bul / Find all input has required attribute
			$("label[for='"+$(this).attr('id')+"']").append(" (*)"); // Etiketi bul ve sonuna (*) ekle / Find label and add (*) end of text
		});
	</script>