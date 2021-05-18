# Donwload-File
Download File from url


//Add This Code when Donwloading 
 
        DownloadManager.Request request=new DownloadManager.Request(Uri.parse(editTextUrl.getText().toString().trim()));
        request.setAllowedNetworkTypes(DownloadManager.Request.NETWORK_WIFI |
                DownloadManager.Request.NETWORK_MOBILE)
        request.setTitle("Download");
        request.setDescription("Downloading File....");
        request.allowScanningByMediaScanner();
        request.setNotificationVisibility(DownloadManager.Request.VISIBILITY_VISIBLE_NOTIFY_COMPLETED);
        request.setDestinationInExternalPublicDir(Environment.DIRECTORY_DOWNLOADS,""+System.currentTimeMillis());
        DownloadManager manager=(DownloadManager)getSystemService(Context.DOWNLOAD_SERVICE);
        manager.enqueue(request);
       
