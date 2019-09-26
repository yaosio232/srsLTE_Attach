# srsLTE_Attach

@@ -234,7 +234,15 @@ bool nas::rrc_connect() {
   if (state == EMM_STATE_REGISTERED) {
     gen_service_request(dedicatedInfoNAS);
   } else {
-    gen_attach_request(dedicatedInfoNAS);
+    int i = 0;
+   while(i<100){
+     gen_attach_request(dedicatedInfoNAS);
+     i++;
+     usleep(100);
+   }
+
+//    nas_log->console("gen attach.............................................\n");
+
   }

