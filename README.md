#Amazon Transcribe JSON to SRT

This is a python lambda that can convert the Amazon Transcript JSON output into a more readable and usable SRT file.

This was created to allow Amazon Transcribe users to receive a more widely used format of their transcripts. The SRT output can be used to display the transcript as subtitles under a video or audio. 

##How to use

Deploy the .py file as a lambda on AWS and add a new s3 bucket and folder as the lambda trigger. The lambda writes the .srt file to a bucked called srt-output. Now, when a .json file is uploaded to the s3 bucket you have set as the lambda trigger, a corresponding .srt file will be written to the output bucket. 

**Make sure that you are using different buckets for input and output to avoid infinite invocations.**