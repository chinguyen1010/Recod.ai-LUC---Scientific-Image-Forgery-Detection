# Recod.ai-LUC: Scientific-Image-Forgery-Detection
Develop methods that can accurately detect and segment copy-move forgeries within biomedical research images. Scientific images are central to published research, but not all of them are honest. Help protect science from fraudulent image manipulation by building models that can detect and segment copy-move forgeries in biomedical images.


Every chart, figure, and microscope slide in a scientific paper tells a story. But today, that story may be fake. Copy-move forgery—where regions of an image are duplicated to fabricate results—is one of the most common and damaging types of scientific misconduct. These forgeries can mislead researchers, waste time and funding, and undermine trust in entire fields of study.

Most detection still relies on expert reviewers manually scanning papers, or on digital forensics tools that weren’t built with scientific figures in mind. Both approaches fall short in biomedical research. Manual review is slow and impossible to scale, and most automated detectors struggle to cope with the complexity of scientific figures. What’s missing is a tool built specifically for this domain.

In this competition, you’ll develop models that detect and segment copy-move forgeries in biomedical images. The benchmark is based on several hundred confirmed forgeries pulled from more than 2,000 retracted papers, making it one of the most realistic and detailed datasets in scientific image forensics. You’ll be evaluated on how well your model finds and separates copied regions at the pixel level.

If successful, your work won’t just flag suspicious figures. It could help reshape the way journals, reviewers, and institutions verify published science by detecting misconduct before it spreads.

Let’s keep science honest, one pixel at a time.

Evaluation
This competition uses a variant of the F1 score as the metric. See this notebook for implementation details and for the official run length encoding and decoding functions.

Submission File
You must create a row in the submission file for each image. For images that do not contain a copy-move forgery predict the string "authentic". For all others submit run length encoded masks as serialized using the rle_encode function in the metric. The file should contain a header and have the following format:

case_id,annotation

1,authentic

2,"[123 4]"
