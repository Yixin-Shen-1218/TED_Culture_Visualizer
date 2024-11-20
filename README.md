# TED_Culture_Visualizer

<p align="center">
  <img src="tmvib5V8Nw 0 seq2seq Italian.gif" alt="example from visualization server">
  <br>
  <i>Example output from the visualization code</i>
</p>




The Blender script can be used directly within Blender, which is helpful if you have Blender installed and want to experiment with the visualizer. I recommend using Blender’s UI for a more interactive visualization experience.

You can render a character animation from a set of generated PKL and WAV files.

Required:

- Blender 2.79B (not compatible with Blender 2.8+)
- FFMPEG



First, set configurations in `renderAnimr_expressive.py` script in `poseRender_expressive_Final_use_the_GENEA_mesh.blend`, and run the script at Blender 2.79B.



Then use common like: **'ffmpeg', '-r', '30', '-y', '-i', img_seq, '-i', audio_path,  '-vcodec', 'prores_ks', '-strict', '-2', merged_video_path** to merge the images and audio to video. You can change the frame rate.



Note that we refined rotations for some joints due to the articulation differences between the rigged skeleton and synthesized skeleton by the gesture generation model. It followed https://github.com/ai4r/Gesture-Generation-from-Trimodal-Context and do some modification for the TED-Culture dataset.



## Acknowledgement

The codebase is developed based on [Speech Gesture Generation from the Trimodal Context of Text, Audio, and Speaker Identity](https://github.com/ai4r/Gesture-Generation-from-Trimodal-Context) of Yoon et al.

The visualization mesh is developed based on the mesh in [Genea_Visualizer](https://github.com/TeoNikolov/genea_visualizer/tree/archive_2022) of Kucherenko et al.

