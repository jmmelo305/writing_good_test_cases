# Test Case 1. 
Test Case ID: TC_UPLOAD_001

Title: Verify successful upload of valid MP4 video

Requirements: System must support MP4 video uploads within size, length, and resolution limits

Test Type: Positive

Preconditions:
- User is logged into TikTok
- User is on the video upload screen
- Valid video file is available on the device

Test Steps:
1. Tap the "+" button to open the upload screen
2. Tap "Upload" to select a video from the device
3. Select valid_video.mp4
4. Verify video preview loads
5. Tap "next"
6. Add a caption
7. Tap "Post"

Test Data:
- File Name: valid_video.mp4
- Format: MP4
- Size: 50 MB
- Length: 30 seconds
- Resolution: 1080 x 1920
- Aspect Ratio: 9:16
- Caption: "Valid upload Test"

Expected Result:
- Video uploads successfully
- Processing completes without error
- Video appears on the user's profile

Priority: High


# Test Case 2.
Test Case ID: TC_UPLOAD_002

Title: Verify upload of minimum length video (3 seconds)

Requirements: Video length must be at least 3 seconds

Test Type: Positive

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Select min_length.mp4 from device storage
2. Tap "Post"

Test Data: 
- Format: MP4
- Size: 3 MB
- Length: 3 seconds
- Resolution: 1080 x 1920

Expected Result: 
- Video uploads and posts successfully

Priority: High

# Test Case 3.
Test Case ID: TC_UPLOAD_003

Title: Upload fails when file size exceeds 287 MB

Requirement: System must reject videos larger than maximum size

Test Type: Negative 

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Select "large_video.MP4"
2. Attempt to upload

Test Data: 
- Size: 300 MB

Expected Result: 
- Upload Fails
- Error message for file size limit is shown

Priority: High

# Test Case 4.
Test Case ID: TC_UPLOAD_004

Title: Upload fails for unsupported video format

Requirement: Only supported formats must be accepted

Test Type: Negative

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Select "video.mkv"

Test Data: 
- Format: MKV

Expected Result: 
- Upload fails
- Error message indicating unsupported format is shown

Priority: High

# Test Case 5.
Test Case ID: TC_UPLOAD_005

Title: Upload video at maximum file size boundary (287 MB)

Requirement: Maximum file size boundary validation

Test Type: Boundary

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Select "max_size.mp4"
2. Tap "post"

Test Data: 
- Size: 287 MB
- Format: MP4

Expected Result: 
- Video uploads successfully

Priority: High

# Test Case 6.
Test Case ID: TC_UPLOAD_006

Title: Upload caption exceeding maximum character limit

Requirement: Caption must not exceed 2,200 characters

Test Type: Boundary 

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Upload a valid video
2. Enter a caption of 2,201 characters
3. Attempt to post

Test Data: 
- Caption Length: 2,201 characters

Expected Result: 
- Caption is rejected
- Error message is shown "too many characters"

Priority: Medium

# Test Case 7.
Test Case ID: TC_UPLOAD_007

Title: Upload valid video without adding effects or filters

Requirement: Effects and filters are optional

Test Type: Black Box

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Upload a valid video
2. Skip effects and filters
3. Tap "Post"

Test Data: 
- No effects or filters applied

Expected Result: 
- Video uploads successfully

Priority: Medium

# Test Case 8.
Test Case ID: TC_UPLOAD_008

Title: Upload valid video and verify feed playback

Requirement: Uploaded videos must be playable in the feed

Test Type: Black Box

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Upload a valid video
2. Navigate to the feed
3. Play the uploaded video

Test Data: 
- Format: MP4
- Length: 45 seconds

Expected Result: 
- Video plays correctly without errors

Priority: Medium

# Test Case 9.
Test Case ID: TC_UPLOAD_009

Title: Upload video with maximum allowed hastags

Requirement: Maximum of 30 hastags allowed 

Test Type: Edge Case

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Upload a valid video
2. Add 30 hastags
3. Tap "post"

Test Data: 
- Hastags: 30 hastags

Expected Result: 
- Video uploads successfully
- All hashtags are saved

Priority: Medium

# Test Case 10.
Test Case ID: TC_UPLOAD_010

Title: Upload corrupted video file

Requirement: System must handle corrupted files properly

Test Type: Edge Case

Preconditions: 
- User is logged in
- User is on the upload screen

Test Steps: 
1. Select "corrupted_file.mp4"
2. Attempt to upload

Test Data: 
- File States: Corrupted

Expected Result: 
- Upload fails
- Error message indicating file cannot be processed is shown

Priority: High